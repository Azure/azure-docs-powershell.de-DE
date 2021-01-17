---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
ms.openlocfilehash: 315a44b986317157a0ada22955c04ea01726327a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471963"
---
# <span data-ttu-id="a5a6e-101">New-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="a5a6e-101">New-AzSentinelDataConnector</span></span>

## <span data-ttu-id="a5a6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5a6e-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a6e-103">Erstellen Sie einen Datenconnector.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-103">Create a Data Connector.</span></span>

## <span data-ttu-id="a5a6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5a6e-104">SYNTAX</span></span>

### <span data-ttu-id="a5a6e-105">AzureActiveDirectory (Standard)</span><span class="sxs-lookup"><span data-stu-id="a5a6e-105">AzureActiveDirectory (Default)</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureActiveDirectory] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5a6e-106">AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="a5a6e-106">AzureAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5a6e-107">AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="a5a6e-107">AzureSecurityCenter</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureSecurityCenter] -Alerts <String> -SubscriptionId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5a6e-108">AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="a5a6e-108">AmazonWebServicesCloudTrail</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AmazonWebServicesCloudTrail] -AwsRoleArn <String> -Logs <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5a6e-109">MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="a5a6e-109">MicrosoftCloudAppSecurity</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftCloudAppSecurity] -Alerts <String> -DiscoveryLogs <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5a6e-110">MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="a5a6e-110">MicrosoftDefenderAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftDefenderAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5a6e-111">Office 365</span><span class="sxs-lookup"><span data-stu-id="a5a6e-111">Office365</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-Office365] -Exchange <String> -SharePoint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5a6e-112">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="a5a6e-112">ThreatIntelligence</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-ThreatIntelligence] -Indicators <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5a6e-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5a6e-113">DESCRIPTION</span></span>
<span data-ttu-id="a5a6e-114">Das **Cmdlet "New-AzSentinelAlertRule"** erstellt eine analytische (Warnungsregel) im angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-114">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="a5a6e-115">Sie müssen einen der Parameter angeben, z. B. "-AzureActiveDirectory", um die Art der zu erstellende Warnungsregel anzugeben.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-115">You must specify one of the parameters, for example -AzureActiveDirectory, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="a5a6e-116">Jede Art hat unterschiedliche erforderliche Parameter.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-116">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="a5a6e-117">Sie können den Parameter *"Bestätigen"* und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-117">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="a5a6e-118">Hinweis: Nicht alle im Portal verfügbaren Datenconnectors sind über API verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-118">Note:  Not all data connectors available in the portal are avaialble via API.</span></span>

## <span data-ttu-id="a5a6e-119">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a5a6e-119">EXAMPLES</span></span>

### <span data-ttu-id="a5a6e-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a5a6e-120">Example 1</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AzureSecurityCenter -Alerts Enabled -SubscriptionId ((Get-AzContext).Subscription.Id)
```

<span data-ttu-id="a5a6e-121">In diesem Beispiel wird ein **DataConnector** für Azure Security Center im angegebenen Arbeitsbereich erstellt und dann in der $DataConnector gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-121">This example creates a **DataConnector** for Azure Security Center in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

### <span data-ttu-id="a5a6e-122">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a5a6e-122">Example 2</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftCloudAppSecurity -Alerts Enabled -DiscoveryLogs Disabled
```

<span data-ttu-id="a5a6e-123">In diesem Beispiel wird ein **DataConnector** für Microsoft Cloud App Security im angegebenen Arbeitsbereich erstellt und dann in der $DataConnector gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-123">This example creates a **DataConnector** for Microsoft Cloud App Security in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="a5a6e-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5a6e-124">PARAMETERS</span></span>

### <span data-ttu-id="a5a6e-125">-Alerts</span><span class="sxs-lookup"><span data-stu-id="a5a6e-125">-Alerts</span></span>
<span data-ttu-id="a5a6e-126">Benachrichtigungen für Datenconnector</span><span class="sxs-lookup"><span data-stu-id="a5a6e-126">Data Connector Alerts</span></span>

```yaml
Type: System.String
Parameter Sets: AzureActiveDirectory, AzureAdvancedThreatProtection, AzureSecurityCenter, MicrosoftCloudAppSecurity, MicrosoftDefenderAdvancedThreatProtection
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-127">-AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="a5a6e-127">-AmazonWebServicesCloudTrail</span></span>
<span data-ttu-id="a5a6e-128">Data Connector Amazon Web Services Cloud Trail</span><span class="sxs-lookup"><span data-stu-id="a5a6e-128">Data Connector Amazon Web Services Cloud Trail</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-129">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="a5a6e-129">-AwsRoleArn</span></span>
<span data-ttu-id="a5a6e-130">Data Connector AWS RoleConnector</span><span class="sxs-lookup"><span data-stu-id="a5a6e-130">Data Connector AWS Role Arn</span></span>

```yaml
Type: System.String
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-131">-AzureActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="a5a6e-131">-AzureActiveDirectory</span></span>
<span data-ttu-id="a5a6e-132">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="a5a6e-132">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureActiveDirectory
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-133">-AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="a5a6e-133">-AzureAdvancedThreatProtection</span></span>
<span data-ttu-id="a5a6e-134">Data Connector Azure Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="a5a6e-134">Data Connector Azure Advanced Threat Protection</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureAdvancedThreatProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-135">-AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="a5a6e-135">-AzureSecurityCenter</span></span>
<span data-ttu-id="a5a6e-136">Data Connector Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="a5a6e-136">Data Connector Azure Security Center</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureSecurityCenter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-137">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="a5a6e-137">-DataConnectorId</span></span>
<span data-ttu-id="a5a6e-138">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="a5a6e-138">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a6e-139">-DefaultProfile</span></span>
<span data-ttu-id="a5a6e-140">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-141">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="a5a6e-141">-DiscoveryLogs</span></span>
<span data-ttu-id="a5a6e-142">Data Connector Discovery Logs</span><span class="sxs-lookup"><span data-stu-id="a5a6e-142">Data Connector Discovery Logs</span></span>

```yaml
Type: System.String
Parameter Sets: MicrosoftCloudAppSecurity
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-143">-Exchange</span><span class="sxs-lookup"><span data-stu-id="a5a6e-143">-Exchange</span></span>
<span data-ttu-id="a5a6e-144">Exchange für Datenconnector</span><span class="sxs-lookup"><span data-stu-id="a5a6e-144">Data Connector Exchange</span></span>

```yaml
Type: System.String
Parameter Sets: Office365
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-145">-Indikatoren</span><span class="sxs-lookup"><span data-stu-id="a5a6e-145">-Indicators</span></span>
<span data-ttu-id="a5a6e-146">Data Connector Indicators</span><span class="sxs-lookup"><span data-stu-id="a5a6e-146">Data Connector Indicators</span></span>

```yaml
Type: System.String
Parameter Sets: ThreatIntelligence
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-147">-Logs</span><span class="sxs-lookup"><span data-stu-id="a5a6e-147">-Logs</span></span>
<span data-ttu-id="a5a6e-148">Datenconnectorprotokolle</span><span class="sxs-lookup"><span data-stu-id="a5a6e-148">Data Connector Logs</span></span>

```yaml
Type: System.String
Parameter Sets: AmazonWebServicesCloudTrail
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-149">-MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="a5a6e-149">-MicrosoftCloudAppSecurity</span></span>
<span data-ttu-id="a5a6e-150">Datenconnector Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="a5a6e-150">Data Connector Microsoft Cloud App Security</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftCloudAppSecurity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-151">-MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="a5a6e-151">-MicrosoftDefenderAdvancedThreatProtection</span></span>
<span data-ttu-id="a5a6e-152">Data Connector Microsoft Defender Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="a5a6e-152">Data Connector Microsoft Defender Advanced Threat Protection</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: MicrosoftDefenderAdvancedThreatProtection
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-153">-Office365</span><span class="sxs-lookup"><span data-stu-id="a5a6e-153">-Office365</span></span>
<span data-ttu-id="a5a6e-154">Datenconnector Office 365</span><span class="sxs-lookup"><span data-stu-id="a5a6e-154">Data Connector Office 365</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Office365
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a6e-155">-ResourceGroupName</span></span>
<span data-ttu-id="a5a6e-156">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="a5a6e-156">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-157">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="a5a6e-157">-SharePoint</span></span>
<span data-ttu-id="a5a6e-158">Data Connector SharePoint</span><span class="sxs-lookup"><span data-stu-id="a5a6e-158">Data Connector SharePoint</span></span>

```yaml
Type: System.String
Parameter Sets: Office365
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a5a6e-159">-SubscriptionId</span></span>
<span data-ttu-id="a5a6e-160">Datenconnector-Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="a5a6e-160">Data connector Subscription Id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSecurityCenter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-161">-ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="a5a6e-161">-ThreatIntelligence</span></span>
<span data-ttu-id="a5a6e-162">Data Connector Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="a5a6e-162">Data Connector Threat Intelligence</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ThreatIntelligence
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-163">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a5a6e-163">-WorkspaceName</span></span>
<span data-ttu-id="a5a6e-164">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="a5a6e-164">Data Connector Azure Active Directory</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5a6e-165">-Confirm</span></span>
<span data-ttu-id="a5a6e-166">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-166">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-167">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a5a6e-167">-WhatIf</span></span>
<span data-ttu-id="a5a6e-168">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5a6e-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-169">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a6e-170">CommonParameters</span></span>
<span data-ttu-id="a5a6e-171">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a6e-172">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a5a6e-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a6e-173">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a5a6e-173">INPUTS</span></span>

### <span data-ttu-id="a5a6e-174">Keine</span><span class="sxs-lookup"><span data-stu-id="a5a6e-174">None</span></span>
## <span data-ttu-id="a5a6e-175">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a5a6e-175">OUTPUTS</span></span>

### <span data-ttu-id="a5a6e-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="a5a6e-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="a5a6e-177">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a5a6e-177">NOTES</span></span>

## <span data-ttu-id="a5a6e-178">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a5a6e-178">RELATED LINKS</span></span>
