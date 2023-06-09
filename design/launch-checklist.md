# Launch Checklist

## Analytics

- [ ] The game uses analytics to track:
  - [ ] Player activity
  - [ ] Monetization
  - [ ] Game economics
  - [ ] Feature utilization
  - [ ] Funnel analysis
  - [ ] Anomalous result tracking
  - [ ] Service performance

## Builds

- [ ] An automated build process exists that doesn't require human interaction.
- [ ] The build process is well-documented.
- [ ] Deployments are fully automated.
- [ ] All needed tests are in place to ensure safe deployments.
- [ ] A branching/labeling process is documented and enforced.
- [ ] There is a promotion process in place for builds to move from development
      into other environments.
- [ ] A notification system is in place to make players aware a new build is
      available for download.
- [ ] Forced version deprecation is in place to ensure security updates must be
      installed before players can start new games (if multiplayer is enabled).
- [ ] Promoting from development requires including patch notes.
- [ ] Promoting to production minimizes downtime.

## Game Client

### Configuration

- [ ] Players can configure the game client to support their preferences,
      system, and accessibility needs.
  - [ ] Windowed, full-windowed, and full-screen modes.
  - [ ] Graphics resolution.
  - [ ] Volume for music, sound effects, environmental noises, and speech.
  - [ ] Sub-titles.
  - [ ] Game controls.

### Region Configuration

- [ ] Players should be able to select the datacenter that will give them the
      best play experience.
- [ ] A QoS system identifies the best datacenter for the player.

### Error Handling

- [ ] Developers should be able to identify the specific location of an error
      from a screenshot.
- [ ] Errors should include a numeric or text code that allows developers to
      locate the offending code.
  - [ ] It is better if the code is easy to understand, like an animal.
- [ ] Error conditions should be easy to identify (e.g. connectivity vs
      connection refused).
- [ ] Support reconnect after disconnect wherever possible.
- [ ] Degrade non-critical systems gracefully.
- [ ] Provide some form of notification to the user when degraded experiences
      occur (low frame rate, low memory, latency, etc).

## Backend

### Persistence

- [ ] Store obfuscated data securely.
- [ ] Do not store player-identifying information.
- [ ] Regularly backup data **to a different location**.
- [ ] Regularly validate backup integrity and the restoration process.
- [ ] Ensure runbooks for restoration and rollbacks are regularly validated and
      tested.

### Capacity

- [ ] Coordinate with cloud service provider (CSP) to ensure needed capacity is
      in place.

### Change Management (CM)

- [ ] Configuration changes are validated automatically before being
      implemented.

### Monitoring

- [ ] Critical processes are monitored and have defined SLAs.
- [ ] Alerts are fired and support people are paged when SLAs are breached.
- [ ] Health metrics are published for internal and external users where
      appropriate.

### Logging

- [ ] Players are not identified using PII (email, name, address, etc.); a
      custom ID is used.
- [ ] The mapping between custom ID and actual player PII is **not** stored
      anywhere except on the player's device.
- [ ] No identifying information is included in logs.
  - [ ] Custom ID can be included for troubleshooting.

### Scaling

- [ ] Scaling is fully automatic.
- [ ] The administrator should only need to change the number of desired hosts
      to initiate scaling activities.
- [ ] Service rate-limit incoming requests.
- [ ] Reconnect attempts use backoff/retry logic.

### Availability

- [ ] Support for configurable availability hours.
- [ ] Ability to set maintenance hours.
- [ ] If needed, a queueing mechanism is in place.
- [ ] If needed, a maximum number of players per server can be configured.
- [ ] If needed, a mechanism to migrate players between servers when requested.
- [ ] If needed, a mechanism to merge servers and players.

### Operations

- [ ] Each procedure/mechanism has a runbook.
- [ ] Runbooks are tested before go-live.
- [ ] On-call engineers are trained to handle common procedures.
- [ ] Escalation path is defined for each runbook.
- [ ] Rollbacks are automated as "single-click" processes.

### Crashes

- [ ] Game clients can report crashes.
- [ ] Crash reporting services are tested to handle load for when large-scale
      issues occur.
- [ ] Crash reporting services include metrics and reporting of frequent/recent
      problems.
- [ ] Crash reports contain relevant log dumps to help in reproduction.
- [ ] Crash reporting services are accessible by on-call/support staff.

## Communication

- [ ] The game should have communication channels for staff.
  - [ ] Message of the day.
  - [ ] Chat broadcasts by language, region, and channel.
  - [ ] Status pages.
  - [ ] Social media.
  - [ ] Maintenance/outage event messages.
  - [ ] Localization procedures for new messages.
- [ ] Players should be able to quickly see if the game is down.

## Support

### KB and Ticket System

- [ ] For issues that players can resolve themselves, there is a knowledge-base
      (KB) with self-help information.
- [ ] The KB system includes analytics on frequently searched issues so that new
      articles can be developed.
- [ ] The KB system links to a ticketing system for issues that are not
      self-service.

### Support Staff

- [ ] Support training covers anticipated game, technical, and billing issues.
- [ ] Support staff are able to provide some reasonable compensation to unduly
      affected players.
- [ ] Support staff are able to track and ban abusive players.
- [ ] Escalation plans exist for harassment, stalking, or other hostile actions.

### Support Tools

- [ ] Tools exist for support staff to correct player account problems across
      all involved services.
- [ ] Tools support making corrections while the player is actively playing.
- [ ] Actions made by support staff in tools are audited and tracked.
- [ ] If needed, tools support making emergency rollbacks to individual player
      inventories.
- [ ] Automated tools exist to track and report on suspected abusive behavior in
      chat.
- [ ] Tools exist to limit player behavior, such as disabling social
      capabilities.
- [ ] A defined escalation path exists to handle abusive player behavior.
- [ ] Player bans/restrictions take effect immediately.
- [ ] Players should be able to see the reason they are banned/limited.

### Player Tools

- [ ] Game clients collect common diagnostics for use in support tickets.
- [ ] Players can submit support tickets both inside and outside the game
      client.
- [ ] Players can report other players for abusive behavior.
- [ ] Players can block social features, as well as individual players.

## Legal

### Ratings

- [ ] The game is rated by the ESRB in North America.
- [ ] The game is rated by the PEGI in Europe.
- [ ] The game adheres to licensing restrictions associated with the provided
      ratings.
- [ ] If the game is rated more mature, age-gating exists for game sites and
      social channels.

### Licenses

- [ ] The game represents all logos, copyrights, patents, trademarks, and
      licenses associated with the game.
- [ ] If required by the third party, the game includes mentions of their
      tools/software in marketing materials and social channels.

### EULA

- [ ] The EULA may need covenants for third-party and/or open source software,
      such as DirectX and Visual Studio Runtime.
- [ ] Players must accept the EULA before playing the game, and any time it is
      updated.

### Other

- [ ] The game follows legal requirements for accessibility (ADA).
- [ ] The game follows legal protections for children (COPA and COPPA).
- [ ] The game website includes a privacy policy.

## Marketing

- [ ] The game and website support email signups.
- [ ] The game supports a "kiosk mode" that doesn't require players to create an
      account (for use at demos/trade shows/etc.).

### Referrals and Engagement

- [ ] The game has a referral system to reward players for bringing in new
      players.
- [ ] The game tracks the source of customer acquisition.
- [ ] The game provides VIP benefits for big spenders/long-time players.
- [ ] The game provides unique benefits for early adopters.
- [ ] There is a review process for inclusion of new items.
  - [ ] Price and game economy impact (if needed).
  - [ ] Cultural issues.
  - [ ] Accessibility issues.

## KPIs

- [ ] Business, operational, and technical metrics are tracked, reported, and
      available in dashboards.
- [ ] Game KPIs
  - [ ] Network latency
  - [ ] Frame rates
  - [ ] Message queues
  - [ ] Server utilization
  - [ ] Server tick rates
  - [ ] Disconnects
  - [ ] Server crashes
  - [ ] Game crashes
  - [ ] Level/match completion rates
- [ ] Business KPIs
  - [ ] Player count
  - [ ] DAU, MAU
  - [ ] Conversion
  - [ ] Revenue
  - [ ] Currency earned
  - [ ] Currency spent
  - [ ] XP/levels earned
  - [ ] Session length
  - [ ] Retention
  - [ ] Usage of features, behaviors, and menu items
  - [ ] Language choices
  - [ ] Region choices
  - [ ] CSP costs

## Experience

### Installation

- [ ] Ask as few questions as possible to complete the install.
- [ ] Give players a choice to install or customize, and be opinionated.
- [ ] Validate and warn against minimum system requirements.
  - [ ] The game is "playable" on a min-spec machine.
- [ ] The installer plans for common errors and helps users succeed.
  - [ ] Examples include disk space, RAM, video drivers, resolution, etc.
- [ ] The installation does not require a reboot.
- [ ] Consult the below guides.
  - [Patching game software in Windows](https://msdn.microsoft.com/en-us/library/windows/desktop/ee418715%28v=vs.85%29.aspx)
  - [Installation Best Practices for MMOs](https://msdn.microsoft.com/en-us/library/windows/desktop/ee418665%28v=vs.85%29.aspx)
  - [Microsoft game installation best practices](https://msdn.microsoft.com/en-us/library/windows/desktop/ee418797%28v=vs.85%29.aspx)
  - [Games for Windows Technical Requirements: Best Practices](https://msdn.microsoft.com/en-us/library/windows/desktop/ee417691%28v=vs.85%29.aspx)
- [ ] The installation folder should be easy to navigate and minimalist.
- [ ] The installation should account for limited vs administrative users
      attempting to install.
- [ ] The installer accounts for common issues such as:
  - [ ] File/directory name conflicts.
  - [ ] Disk running out of space.
  - [ ] Installation on a secondary drive.
  - [ ] File/directory permission changes during installation.
  - [ ] SSL certificate issues.
  - [ ] Duplicate installers running.
- [ ] The game does not depend on the Windows registry.

### Uninstallation

- [ ] The uninstaller does not use wildcard deletes.
- [ ] The game uses an uninstall list to track what files to remove.
- [ ] The uninstaller uninstalls the uninstaller.

### Patching

- [ ] Patches are small in both size and disk writing required.
- [ ] Players can see the size of patches before installing.
- [ ] Players can control background patching time.
- [ ] Players do not need admin rights to patch.
- [ ] Patch code is signed before being executed.

### Launcher

- [ ] Launcher does not run with administrative permissions (though it might
      need admin rights to be installed).

### Testing

- [ ] Fuzz testing is implemented as part of the build process.
- [ ] Load testing is implemented as part of the build process.
- [ ] High/variable latency can be configured in non-prod environments for
      testing.
- [ ] Canaries exist to detect and alert on failure.

## Localization

- [ ] Libraries are included for localization to parse, calculate, and display
      strings, numbers, times, dates, and timezones.
- [ ] Code does not assume grammar when formatting text.
- [ ] The game supports switching between at least two languages for
      localization testing.
- [ ] Localization includes multiple forms of the same language (US/UK English).
- [ ] Player language is detected from the OS, but can be changed.
- [ ] Prepared messages exist for common communication such as outages and
      maintenance.
- [ ] Localizable resources are stored in a separate directory structure from
      non-localizable resources.
- [ ] Support throughout for UTF-8 (game, docs, web, etc.).
- [ ] The game UI supports dynamically sizing text resources horizontally and
      vertically, with word-wrapping.
- [ ] The game does not use abbreviations.
- [ ] Localized text is not included in textures.

## Security

### Incident Awareness

- [ ] A security page exists to inform players of common security issues.
- [ ] A security reporting page exists for players to report issues.

### Asset Security

- [ ] Server source and binaries are not available to end-users.
- [ ] Server and client source code are separate from one another.

### Network Security

- [ ] Messages across any network are signed and encrypted.
- [ ] Messages are semantically evaluated before being processed.
- [ ] Invalid messages are logged for tracking of high corruption rates (common
      with malicious users).
- [ ] All endpoints are fuzz-tested.
- [ ] No hardcoded keys, passwords, or other risky data on servers or clients.
- [ ] DoS mitigation in place (rate-limiting).
- [ ] Communication port to servers is randomized to reduce DDOS attempts.

### Player Accounts

- [ ] New player accounts are temporarily limited to prevent smurfing.
- [ ] Common forms of cheating, griefing, etc. are mitigated.
- [ ] Limits are in place to mitigate fencing.
- [ ] The game has limits/throttles on player behaviors.
- [ ] Chat filtering, enabled by default, limits profane words.
- [ ] Player names are validated against profanity, trademarks, celebrities,
      etc.
- [ ] Players can report and block other players.

### Code Signing

- [ ] All downloadable code binaries/executables/DLLs should be electronically
      signed.
- [ ] Signatures should be verified to prevent code injection.
