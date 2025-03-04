# Mythic Progress Bar Enhanced

This is a forked and enhanced version of the original Mythic Progress Bar resource, now offering a more engaging and responsive progress bar for your FiveM server. Originally tailored for the IRAN ROLEPLAY server—now offline for nearly 2 years—these improvements have been refined and are now available on GitHub for the community.

## Overview

The enhancements are implemented in two main phases:

1. **Visual Enhancements**  
   - **Improved Styles & Functionality:** Adjusted dimensions, colors, and animations for better visibility and a modern look.
   - **Enhanced User Experience:** Smoother animations and a more attractive interface.

2. **Code Improvements**  
   - **Refactored Lua Implementation:** Streamlined the progress bar code for efficiency.
   - **Resource Manifest Removal:** Cleaned up the resource manifest for a leaner setup.
   - **Enhanced Event Handling:** New event handlers and improved client script functionality for better action management.

## How To Use

Simply trigger the event in your client script where you need the progress bar. Here’s an example of how to call the event:

```lua
TriggerEvent("mythic_progbar:client:progress", {
    name = "unique_action_name",
    duration = 10000,
    label = "Action Label",
    useWhileDead = false,
    canCancel = true,
    controlDisables = {
        disableMovement = true,
        disableCarMovement = true,
        disableMouse = false,
        disableCombat = true,
    },
    animation = {
        animDict = "missheistdockssetup1clipboard@idle_a",
        anim = "idle_a",
    },
    prop = {
        model = "prop_paper_bag_small",
    }
}, function(status)
    if not status then
        -- Do Something If Event Wasn't Cancelled
    end
end)