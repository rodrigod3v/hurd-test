# Manual & Exploratory Test Scenarios - Hurd App

## 1. Manual Test Cases (Focus Areas)

### Area: Community Feed
| ID | Title | Steps | Expected Result |
|---|---|---|---|
| CF-01 | Create Text Post | 1. Go to Feed<br>2. Click "Create"<br>3. Type text<br>4. Post | Post appears at the top of the feed. |
| CF-02 | Create Post with Image | 1. Go to Feed<br>2. Click "Create"<br>3. Upload image<br>4. Post | Post displays image correctly without distortion. |
| CF-03 | Like/React to Post | 1. Find a post<br>2. Click "Like" | Counter increments and icon changes state. |
| CF-04 | Feed Refresh | 1. Scroll down<br>2. Pull to refresh | Feed updates and loading indicators disappear. |

### Area: Learning Content
| ID | Title | Steps | Expected Result |
|---|---|---|---|
| LC-01 | Start Lesson | 1. Go to Learning<br>2. Select a lesson<br>3. Click "Start" | Lesson screen opens with correct content. |
| LC-02 | Lesson Navigation | 1. Open lesson<br>2. Click "Next" through slides | Smooth transitions between content slides. |
| LC-03 | Completion Tracking | 1. Finish all slides<br>2. Check Progress | Completion status reflects 100% or "Finished". |

---

## 2. Exploratory Testing Charter

**Target**: Resilience and UX Edge Cases
**Timebox**: 30-45 minutes

### Missions:
1.  **Network Resilience**: 
    - Switch to Airplane mode while a video lesson is playing.
    - Post to feed with a very slow 3G connection (use Emulator throttling).
2.  **App State Interruptions**:
    - Minimize app during a rating submission and return.
    - Receive a notification/call while in the middle of a lesson.
3.  **UI/UX Stress**:
    - Input extremely long strings in the post creation (1000+ chars).
    - Rapidly tap "Like" button multiple times.
    - Test dark mode vs light mode switching on different screens.
4.  **Navigation Deepness**:
    - Try to find "Dead Ends" (screens with no back button).
    - Navigate rapidly between Feed and Learning to check for memory leaks/crashes.
