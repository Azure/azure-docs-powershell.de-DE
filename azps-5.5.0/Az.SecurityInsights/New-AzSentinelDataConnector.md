---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelDataConnector.md
ms.openlocfilehash: 315a44b986317157a0ada22955c04ea01726327a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168964"
---
# <span data-ttu-id="afb08-101">New-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="afb08-101">New-AzSentinelDataConnector</span></span>

## <span data-ttu-id="afb08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afb08-102">SYNOPSIS</span></span>
<span data-ttu-id="afb08-103">Erstellen Sie einen Datenconnector.</span><span class="sxs-lookup"><span data-stu-id="afb08-103">Create a Data Connector.</span></span>

## <span data-ttu-id="afb08-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afb08-104">SYNTAX</span></span>

### <span data-ttu-id="afb08-105">AzureActiveDirectory (Standard)</span><span class="sxs-lookup"><span data-stu-id="afb08-105">AzureActiveDirectory (Default)</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureActiveDirectory] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="afb08-106">AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="afb08-106">AzureAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afb08-107">AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="afb08-107">AzureSecurityCenter</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AzureSecurityCenter] -Alerts <String> -SubscriptionId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afb08-108">AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="afb08-108">AmazonWebServicesCloudTrail</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-AmazonWebServicesCloudTrail] -AwsRoleArn <String> -Logs <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afb08-109">MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="afb08-109">MicrosoftCloudAppSecurity</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftCloudAppSecurity] -Alerts <String> -DiscoveryLogs <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afb08-110">MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="afb08-110">MicrosoftDefenderAdvancedThreatProtection</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-MicrosoftDefenderAdvancedThreatProtection] -Alerts <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afb08-111">Office 365</span><span class="sxs-lookup"><span data-stu-id="afb08-111">Office365</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-Office365] -Exchange <String> -SharePoint <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="afb08-112">ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="afb08-112">ThreatIntelligence</span></span>
```
New-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> [-DataConnectorId <String>]
 [-ThreatIntelligence] -Indicators <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="afb08-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="afb08-113">DESCRIPTION</span></span>
<span data-ttu-id="afb08-114">Das **Cmdlet "New-AzSentinelAlertRule"** erstellt eine analytische (Warnungsregel) im angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="afb08-114">The **New-AzSentinelAlertRule** cmdlet creates an Analytic (Alert Rule) in the specified workspace.</span></span>
<span data-ttu-id="afb08-115">Sie müssen einen der Parameter angeben, z. B. "-AzureActiveDirectory", um die Art der zu erstellende Warnungsregel anzugeben.</span><span class="sxs-lookup"><span data-stu-id="afb08-115">You must specify one of the parameters, for example -AzureActiveDirectory, to specify the kind of Alert rule to create.</span></span>  <span data-ttu-id="afb08-116">Jede Art hat unterschiedliche erforderliche Parameter.</span><span class="sxs-lookup"><span data-stu-id="afb08-116">Each Kind has different required paramaters.</span></span>
<span data-ttu-id="afb08-117">Sie können den Parameter *"Bestätigen"* und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="afb08-117">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="afb08-118">Hinweis: Nicht alle im Portal verfügbaren Datenconnectors sind über API verfügbar.</span><span class="sxs-lookup"><span data-stu-id="afb08-118">Note:  Not all data connectors available in the portal are avaialble via API.</span></span>

## <span data-ttu-id="afb08-119">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="afb08-119">EXAMPLES</span></span>

### <span data-ttu-id="afb08-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="afb08-120">Example 1</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -AzureSecurityCenter -Alerts Enabled -SubscriptionId ((Get-AzContext).Subscription.Id)
```

<span data-ttu-id="afb08-121">In diesem Beispiel wird **ein DataConnector** für Azure Security Center im angegebenen Arbeitsbereich erstellt und dann in der $DataConnector gespeichert.</span><span class="sxs-lookup"><span data-stu-id="afb08-121">This example creates a **DataConnector** for Azure Security Center in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

### <span data-ttu-id="afb08-122">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="afb08-122">Example 2</span></span>
```powershell
PS C:\> $DataConnector = New-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -MicrosoftCloudAppSecurity -Alerts Enabled -DiscoveryLogs Disabled
```

<span data-ttu-id="afb08-123">In diesem Beispiel wird ein **DataConnector** für Microsoft Cloud App Security im angegebenen Arbeitsbereich erstellt und dann in der $DataConnector gespeichert.</span><span class="sxs-lookup"><span data-stu-id="afb08-123">This example creates a **DataConnector** for Microsoft Cloud App Security in the specified workspace, and then stores it in the $DataConnector variable.</span></span>

## <span data-ttu-id="afb08-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afb08-124">PARAMETERS</span></span>

### <span data-ttu-id="afb08-125">-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="afb08-125">-Alerts</span></span>
<span data-ttu-id="afb08-126">Benachrichtigungen für Datenconnector</span><span class="sxs-lookup"><span data-stu-id="afb08-126">Data Connector Alerts</span></span>

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

### <span data-ttu-id="afb08-127">-AmazonWebServicesCloudTrail</span><span class="sxs-lookup"><span data-stu-id="afb08-127">-AmazonWebServicesCloudTrail</span></span>
<span data-ttu-id="afb08-128">Data Connector Amazon Web Services Cloud Trail</span><span class="sxs-lookup"><span data-stu-id="afb08-128">Data Connector Amazon Web Services Cloud Trail</span></span>

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

### <span data-ttu-id="afb08-129">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="afb08-129">-AwsRoleArn</span></span>
<span data-ttu-id="afb08-130">Data Connector AWS Role Von</span><span class="sxs-lookup"><span data-stu-id="afb08-130">Data Connector AWS Role Arn</span></span>

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

### <span data-ttu-id="afb08-131">-AzureActiveDirectory</span><span class="sxs-lookup"><span data-stu-id="afb08-131">-AzureActiveDirectory</span></span>
<span data-ttu-id="afb08-132">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="afb08-132">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="afb08-133">-AzureAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="afb08-133">-AzureAdvancedThreatProtection</span></span>
<span data-ttu-id="afb08-134">Data Connector Azure Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="afb08-134">Data Connector Azure Advanced Threat Protection</span></span>

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

### <span data-ttu-id="afb08-135">-AzureSecurityCenter</span><span class="sxs-lookup"><span data-stu-id="afb08-135">-AzureSecurityCenter</span></span>
<span data-ttu-id="afb08-136">Data Connector Azure Security Center</span><span class="sxs-lookup"><span data-stu-id="afb08-136">Data Connector Azure Security Center</span></span>

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

### <span data-ttu-id="afb08-137">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="afb08-137">-DataConnectorId</span></span>
<span data-ttu-id="afb08-138">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="afb08-138">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="afb08-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afb08-139">-DefaultProfile</span></span>
<span data-ttu-id="afb08-140">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="afb08-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afb08-141">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="afb08-141">-DiscoveryLogs</span></span>
<span data-ttu-id="afb08-142">Data Connector Discovery Logs</span><span class="sxs-lookup"><span data-stu-id="afb08-142">Data Connector Discovery Logs</span></span>

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

### <span data-ttu-id="afb08-143">-Exchange</span><span class="sxs-lookup"><span data-stu-id="afb08-143">-Exchange</span></span>
<span data-ttu-id="afb08-144">Exchange für Datenconnector</span><span class="sxs-lookup"><span data-stu-id="afb08-144">Data Connector Exchange</span></span>

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

### <span data-ttu-id="afb08-145">-Indikatoren</span><span class="sxs-lookup"><span data-stu-id="afb08-145">-Indicators</span></span>
<span data-ttu-id="afb08-146">Data Connector Indicators</span><span class="sxs-lookup"><span data-stu-id="afb08-146">Data Connector Indicators</span></span>

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

### <span data-ttu-id="afb08-147">-Logs</span><span class="sxs-lookup"><span data-stu-id="afb08-147">-Logs</span></span>
<span data-ttu-id="afb08-148">Datenconnectorprotokolle</span><span class="sxs-lookup"><span data-stu-id="afb08-148">Data Connector Logs</span></span>

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

### <span data-ttu-id="afb08-149">-MicrosoftCloudAppSecurity</span><span class="sxs-lookup"><span data-stu-id="afb08-149">-MicrosoftCloudAppSecurity</span></span>
<span data-ttu-id="afb08-150">Datenconnector Microsoft Cloud App Security</span><span class="sxs-lookup"><span data-stu-id="afb08-150">Data Connector Microsoft Cloud App Security</span></span>

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

### <span data-ttu-id="afb08-151">-MicrosoftDefenderAdvancedThreatProtection</span><span class="sxs-lookup"><span data-stu-id="afb08-151">-MicrosoftDefenderAdvancedThreatProtection</span></span>
<span data-ttu-id="afb08-152">Data Connector Microsoft Defender Advanced Threat Protection</span><span class="sxs-lookup"><span data-stu-id="afb08-152">Data Connector Microsoft Defender Advanced Threat Protection</span></span>

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

### <span data-ttu-id="afb08-153">-Office365</span><span class="sxs-lookup"><span data-stu-id="afb08-153">-Office365</span></span>
<span data-ttu-id="afb08-154">Datenconnector Office 365</span><span class="sxs-lookup"><span data-stu-id="afb08-154">Data Connector Office 365</span></span>

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

### <span data-ttu-id="afb08-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afb08-155">-ResourceGroupName</span></span>
<span data-ttu-id="afb08-156">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="afb08-156">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="afb08-157">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="afb08-157">-SharePoint</span></span>
<span data-ttu-id="afb08-158">Data Connector SharePoint</span><span class="sxs-lookup"><span data-stu-id="afb08-158">Data Connector SharePoint</span></span>

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

### <span data-ttu-id="afb08-159">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="afb08-159">-SubscriptionId</span></span>
<span data-ttu-id="afb08-160">Datenconnector-Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="afb08-160">Data connector Subscription Id</span></span>

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

### <span data-ttu-id="afb08-161">-ThreatIntelligence</span><span class="sxs-lookup"><span data-stu-id="afb08-161">-ThreatIntelligence</span></span>
<span data-ttu-id="afb08-162">Data Connector Threat Intelligence</span><span class="sxs-lookup"><span data-stu-id="afb08-162">Data Connector Threat Intelligence</span></span>

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

### <span data-ttu-id="afb08-163">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="afb08-163">-WorkspaceName</span></span>
<span data-ttu-id="afb08-164">Data Connector Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="afb08-164">Data Connector Azure Active Directory</span></span>

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

### <span data-ttu-id="afb08-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afb08-165">-Confirm</span></span>
<span data-ttu-id="afb08-166">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="afb08-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afb08-167">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="afb08-167">-WhatIf</span></span>
<span data-ttu-id="afb08-168">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="afb08-168">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afb08-169">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="afb08-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afb08-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afb08-170">CommonParameters</span></span>
<span data-ttu-id="afb08-171">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afb08-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afb08-172">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="afb08-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afb08-173">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="afb08-173">INPUTS</span></span>

### <span data-ttu-id="afb08-174">Keine</span><span class="sxs-lookup"><span data-stu-id="afb08-174">None</span></span>
## <span data-ttu-id="afb08-175">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="afb08-175">OUTPUTS</span></span>

### <span data-ttu-id="afb08-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="afb08-176">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>
## <span data-ttu-id="afb08-177">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="afb08-177">NOTES</span></span>

## <span data-ttu-id="afb08-178">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="afb08-178">RELATED LINKS</span></span>
