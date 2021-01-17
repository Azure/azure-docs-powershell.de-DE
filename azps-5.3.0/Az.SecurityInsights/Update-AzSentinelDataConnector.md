---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentineldataconnector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelDataConnector.md
ms.openlocfilehash: b998d699836cf99f9d6cb9dc53bef36b6fc94ca3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471938"
---
# <span data-ttu-id="0c7d6-101">Update-AzSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="0c7d6-101">Update-AzSentinelDataConnector</span></span>

## <span data-ttu-id="0c7d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c7d6-102">SYNOPSIS</span></span>
<span data-ttu-id="0c7d6-103">Aktualisieren sie einen Datenconnector.</span><span class="sxs-lookup"><span data-stu-id="0c7d6-103">Update a Data Connector.</span></span>

## <span data-ttu-id="0c7d6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0c7d6-104">SYNTAX</span></span>

### <span data-ttu-id="0c7d6-105">DataConnectorId (Standard)</span><span class="sxs-lookup"><span data-stu-id="0c7d6-105">DataConnectorId (Default)</span></span>
```
Update-AzSentinelDataConnector -ResourceGroupName <String> -WorkspaceName <String> -DataConnectorId <String>
 [-Alerts <String>] [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>]
 [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c7d6-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0c7d6-106">InputObject</span></span>
```
Update-AzSentinelDataConnector -InputObject <PSSentinelDataConnector> [-Alerts <String>]
 [-SubscriptionId <String>] [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>]
 [-Exchange <String>] [-SharePoint <String>] [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c7d6-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c7d6-107">ResourceId</span></span>
```
Update-AzSentinelDataConnector -ResourceId <String> [-Alerts <String>] [-SubscriptionId <String>]
 [-AwsRoleArn <String>] [-Logs <String>] [-DiscoveryLogs <String>] [-Exchange <String>] [-SharePoint <String>]
 [-Indicators <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c7d6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c7d6-108">DESCRIPTION</span></span>
<span data-ttu-id="0c7d6-109">Das **Cmdlet "Update-AzSentinelDataConnector"** aktualisiert den Datenconnector im angegebenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="0c7d6-109">The **Update-AzSentinelDataConnector** cmdlet updates the Data Connector in the specified workspace.</span></span>
<span data-ttu-id="0c7d6-110">Sie können ein **DataConnector-Objekt** als Parameter oder mithilfe des Pipelineoperators übergeben, oder Sie können die erforderlichen Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="0c7d6-110">You can pass an **DataConnector** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="0c7d6-111">Sie können den Parameter *"Bestätigen"* und $ConfirmPreference Windows PowerShell, um zu steuern, ob sie vom Cmdlet zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="0c7d6-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="0c7d6-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0c7d6-112">EXAMPLES</span></span>

### <span data-ttu-id="0c7d6-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0c7d6-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelDataConnector -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -DataConnectorId "MyDataConnectorId" -Alerts Disabled
```

<span data-ttu-id="0c7d6-114">Der Befehl ruft den Datenconnector mit *"DataConnectorId" ab* und legt den *Benachrichtigungszustand* auf *"Deaktiviert" fest.*</span><span class="sxs-lookup"><span data-stu-id="0c7d6-114">The command gets the Data Connector by *DataConnectorId* and sets the *Alerts* state to *Disabled*.</span></span>  <span data-ttu-id="0c7d6-115">Alle anderen Eigenschaften bleiben gleich.</span><span class="sxs-lookup"><span data-stu-id="0c7d6-115">All other properties remain the same.</span></span>

## <span data-ttu-id="0c7d6-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c7d6-116">PARAMETERS</span></span>

### <span data-ttu-id="0c7d6-117">-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="0c7d6-117">-Alerts</span></span>
<span data-ttu-id="0c7d6-118">Benachrichtigungen für Datenconnector</span><span class="sxs-lookup"><span data-stu-id="0c7d6-118">Data Connector Alerts</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7d6-119">-AwsRoleArn</span><span class="sxs-lookup"><span data-stu-id="0c7d6-119">-AwsRoleArn</span></span>
<span data-ttu-id="0c7d6-120">Data Connector AWS Role Von</span><span class="sxs-lookup"><span data-stu-id="0c7d6-120">Data Connector AWS Role Arn</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7d6-121">-DataConnectorId</span><span class="sxs-lookup"><span data-stu-id="0c7d6-121">-DataConnectorId</span></span>
<span data-ttu-id="0c7d6-122">Datenconnector-ID.</span><span class="sxs-lookup"><span data-stu-id="0c7d6-122">Data Connector Id.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7d6-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c7d6-123">-DefaultProfile</span></span>
<span data-ttu-id="0c7d6-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0c7d6-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7d6-125">-DiscoveryLogs</span><span class="sxs-lookup"><span data-stu-id="0c7d6-125">-DiscoveryLogs</span></span>
<span data-ttu-id="0c7d6-126">Data Connector Discovery Logs</span><span class="sxs-lookup"><span data-stu-id="0c7d6-126">Data Connector Discovery Logs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7d6-127">-Exchange</span><span class="sxs-lookup"><span data-stu-id="0c7d6-127">-Exchange</span></span>
<span data-ttu-id="0c7d6-128">Exchange für Datenconnector</span><span class="sxs-lookup"><span data-stu-id="0c7d6-128">Data Connector Exchange</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7d6-129">-Indikatoren</span><span class="sxs-lookup"><span data-stu-id="0c7d6-129">-Indicators</span></span>
<span data-ttu-id="0c7d6-130">Data Connector Indicators</span><span class="sxs-lookup"><span data-stu-id="0c7d6-130">Data Connector Indicators</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7d6-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c7d6-131">-InputObject</span></span>
<span data-ttu-id="0c7d6-132">InputObject.</span><span class="sxs-lookup"><span data-stu-id="0c7d6-132">InputObject.</span></span>

```yaml
Type: PSSentinelDataConnector
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c7d6-133">-Logs</span><span class="sxs-lookup"><span data-stu-id="0c7d6-133">-Logs</span></span>
<span data-ttu-id="0c7d6-134">Datenconnectorprotokolle</span><span class="sxs-lookup"><span data-stu-id="0c7d6-134">Data Connector Logs</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7d6-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c7d6-135">-ResourceGroupName</span></span>
<span data-ttu-id="0c7d6-136">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="0c7d6-136">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7d6-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c7d6-137">-ResourceId</span></span>
<span data-ttu-id="0c7d6-138">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="0c7d6-138">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c7d6-139">-SharePoint</span><span class="sxs-lookup"><span data-stu-id="0c7d6-139">-SharePoint</span></span>
<span data-ttu-id="0c7d6-140">Data Connector SharePoint</span><span class="sxs-lookup"><span data-stu-id="0c7d6-140">Data Connector SharePoint</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7d6-141">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0c7d6-141">-SubscriptionId</span></span>
<span data-ttu-id="0c7d6-142">Datenconnector-Abonnement-ID</span><span class="sxs-lookup"><span data-stu-id="0c7d6-142">Data connector Subscription Id</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7d6-143">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="0c7d6-143">-WorkspaceName</span></span>
<span data-ttu-id="0c7d6-144">Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="0c7d6-144">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: DataConnectorId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7d6-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c7d6-145">-Confirm</span></span>
<span data-ttu-id="0c7d6-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0c7d6-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7d6-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0c7d6-147">-WhatIf</span></span>
<span data-ttu-id="0c7d6-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0c7d6-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c7d6-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c7d6-149">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c7d6-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c7d6-150">CommonParameters</span></span>
<span data-ttu-id="0c7d6-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c7d6-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c7d6-152">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c7d6-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c7d6-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0c7d6-153">INPUTS</span></span>

### <span data-ttu-id="0c7d6-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="0c7d6-154">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

### <span data-ttu-id="0c7d6-155">System.String</span><span class="sxs-lookup"><span data-stu-id="0c7d6-155">System.String</span></span>

## <span data-ttu-id="0c7d6-156">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0c7d6-156">OUTPUTS</span></span>

### <span data-ttu-id="0c7d6-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span><span class="sxs-lookup"><span data-stu-id="0c7d6-157">Microsoft.Azure.Commands.SecurityInsights.Models.DataConnectors.PSSentinelDataConnector</span></span>

## <span data-ttu-id="0c7d6-158">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0c7d6-158">NOTES</span></span>

## <span data-ttu-id="0c7d6-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0c7d6-159">RELATED LINKS</span></span>
