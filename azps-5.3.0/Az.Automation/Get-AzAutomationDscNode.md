---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 6493186F-064B-45B7-8DFD-7799B1F2E5C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNode.md
ms.openlocfilehash: f1328b71564b0fd839d3481a87b23a2a8b24ab55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471374"
---
# <span data-ttu-id="b3d76-101">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b3d76-101">Get-AzAutomationDscNode</span></span>

## <span data-ttu-id="b3d76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3d76-102">SYNOPSIS</span></span>
<span data-ttu-id="b3d76-103">Ruft die DSC-Knoten aus der Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="b3d76-103">Gets DSC nodes from Automation.</span></span>

## <span data-ttu-id="b3d76-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b3d76-104">SYNTAX</span></span>

### <span data-ttu-id="b3d76-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="b3d76-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3d76-106">ById</span><span class="sxs-lookup"><span data-stu-id="b3d76-106">ById</span></span>
```
Get-AzAutomationDscNode -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3d76-107">ByName</span><span class="sxs-lookup"><span data-stu-id="b3d76-107">ByName</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3d76-108">ByNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3d76-108">ByNodeConfiguration</span></span>
```
Get-AzAutomationDscNode [-Status <DscNodeStatus>] -NodeConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b3d76-109">ByConfiguration</span><span class="sxs-lookup"><span data-stu-id="b3d76-109">ByConfiguration</span></span>
```
Get-AzAutomationDscNode -ConfigurationName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3d76-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b3d76-110">DESCRIPTION</span></span>
<span data-ttu-id="b3d76-111">Das **Cmdlet "Get-AzAutomationDscNode"** ruft APS Desired State Configuration (DSC)-Knoten aus der Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="b3d76-111">The **Get-AzAutomationDscNode** cmdlet gets APS Desired State Configuration (DSC) nodes from Azure Automation.</span></span>

## <span data-ttu-id="b3d76-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b3d76-112">EXAMPLES</span></span>

### <span data-ttu-id="b3d76-113">Beispiel 1: Alle -DSC-Knoten erhalten</span><span class="sxs-lookup"><span data-stu-id="b3d76-113">Example 1: Get all DSC nodes</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="b3d76-114">Dieser Befehl ruft Metadaten für alle DSC-Knoten im Automatisierungskonto namens "Contoso17" ab.</span><span class="sxs-lookup"><span data-stu-id="b3d76-114">This command gets metadata for all DSC nodes in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b3d76-115">Beispiel 2: Erhalten aller DSC-Knoten für eine DSC-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="b3d76-115">Example 2: Get all DSC nodes for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="b3d76-116">Dieser Befehl ruft Metadaten für alle DSC-Knoten im Automatisierungskonto namens Contoso17 ab, die einer DSC-Knotenkonfiguration zugeordnet sind, die von der DSC-Konfiguration ContosoConfiguration generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="b3d76-116">This command gets metadata for all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration which was generated by DSC configuration ContosoConfiguration.</span></span>

### <span data-ttu-id="b3d76-117">Beispiel 3: Erhalten eines DSC-Knotens nach ID</span><span class="sxs-lookup"><span data-stu-id="b3d76-117">Example 3: Get a DSC node by ID</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

<span data-ttu-id="b3d76-118">Dieser Befehl ruft Metadaten für einen DSC-Knoten mit der angegebenen ID im Automatisierungskonto namens "Contoso17" ab.</span><span class="sxs-lookup"><span data-stu-id="b3d76-118">This command gets metadata on a DSC node with the specified ID in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b3d76-119">Beispiel 4: Erhalten eines DSC-Knotens nach Name</span><span class="sxs-lookup"><span data-stu-id="b3d76-119">Example 4: Get a DSC node by name</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
```

<span data-ttu-id="b3d76-120">Dieser Befehl ruft Metadaten für einen DSC-Knoten mit dem Namen "Computer14" im Automatisierungskonto namens "Contoso17" ab.</span><span class="sxs-lookup"><span data-stu-id="b3d76-120">This command gets metadata on a DSC node with the name Computer14 in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b3d76-121">Beispiel 5: Erhalten aller DSC-Knoten, die einer Konfiguration des DSC-Knotens zugeordnet sind</span><span class="sxs-lookup"><span data-stu-id="b3d76-121">Example 5: Get all DSC nodes mapped to a DSC node configuration</span></span>
```
PS C:\>Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeConfigurationName "ContosoConfiguration.webserver"
```

<span data-ttu-id="b3d76-122">Dieser Befehl ruft Metadaten für alle DSC-Knoten im Automatisierungskonto namens Contoso17 ab, die einer Konfiguration des DSC-Knotens "ContosoConfiguration.webserver" zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="b3d76-122">This command gets metadata on all DSC nodes in the Automation account named Contoso17 that are mapped to a DSC node configuration named ContosoConfiguration.webserver.</span></span>

## <span data-ttu-id="b3d76-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3d76-123">PARAMETERS</span></span>

### <span data-ttu-id="b3d76-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b3d76-124">-AutomationAccountName</span></span>
<span data-ttu-id="b3d76-125">Gibt den Namen des Automatisierungskontos an, das die VON diesem Cmdlet abgerufenen DSC-Knoten enthält.</span><span class="sxs-lookup"><span data-stu-id="b3d76-125">Specifies the name of the Automation account that contains the DSC nodes that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3d76-126">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b3d76-126">-ConfigurationName</span></span>
<span data-ttu-id="b3d76-127">Gibt den Namen einer DSC-Konfiguration an.</span><span class="sxs-lookup"><span data-stu-id="b3d76-127">Specifies the name of a DSC configuration.</span></span>
<span data-ttu-id="b3d76-128">Dieses Cmdlet ruft DIE DSC-Knoten ab, die den Knotenkonfigurationen entsprechen, die aus der von diesem Parameter angegebenen Konfiguration generiert werden.</span><span class="sxs-lookup"><span data-stu-id="b3d76-128">This cmdlet gets DSC nodes that match the node configurations generated from the configuration that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3d76-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3d76-129">-DefaultProfile</span></span>
<span data-ttu-id="b3d76-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b3d76-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3d76-131">-ID</span><span class="sxs-lookup"><span data-stu-id="b3d76-131">-Id</span></span>
<span data-ttu-id="b3d76-132">Gibt die eindeutige ID des DSC-Knotens an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="b3d76-132">Specifies the unique ID of the DSC node that this cmdlet gets.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3d76-133">-Name</span><span class="sxs-lookup"><span data-stu-id="b3d76-133">-Name</span></span>
<span data-ttu-id="b3d76-134">Gibt den Namen eines DSC-Knotens an, den dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="b3d76-134">Specifies the name of a DSC node that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: NodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3d76-135">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="b3d76-135">-NodeConfigurationName</span></span>
<span data-ttu-id="b3d76-136">Gibt den Namen einer Knotenkonfiguration an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="b3d76-136">Specifies the name of a node configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3d76-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3d76-137">-ResourceGroupName</span></span>
<span data-ttu-id="b3d76-138">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet -Knoten erhält.</span><span class="sxs-lookup"><span data-stu-id="b3d76-138">Specifies the name of a resource group in which this cmdlet gets DSC nodes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3d76-139">-Status</span><span class="sxs-lookup"><span data-stu-id="b3d76-139">-Status</span></span>
<span data-ttu-id="b3d76-140">Gibt den Status der DSC-Knoten an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="b3d76-140">Specifies the status of the DSC nodes that this cmdlet gets.</span></span>
<span data-ttu-id="b3d76-141">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="b3d76-141">Valid values are:</span></span> 
- <span data-ttu-id="b3d76-142">Konform</span><span class="sxs-lookup"><span data-stu-id="b3d76-142">Compliant</span></span> 
- <span data-ttu-id="b3d76-143">NotCompliant</span><span class="sxs-lookup"><span data-stu-id="b3d76-143">NotCompliant</span></span>
- <span data-ttu-id="b3d76-144">Fehler</span><span class="sxs-lookup"><span data-stu-id="b3d76-144">Failed</span></span>
- <span data-ttu-id="b3d76-145">Ausstehend</span><span class="sxs-lookup"><span data-stu-id="b3d76-145">Pending</span></span> 
- <span data-ttu-id="b3d76-146">Received</span><span class="sxs-lookup"><span data-stu-id="b3d76-146">Received</span></span>
- <span data-ttu-id="b3d76-147">Nicht reagieren</span><span class="sxs-lookup"><span data-stu-id="b3d76-147">Unresponsive</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Common.DscNodeStatus
Parameter Sets: ByAll, ByName, ByNodeConfiguration
Aliases:
Accepted values: Compliant, NotCompliant, Failed, Pending, Received, Unresponsive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b3d76-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3d76-148">CommonParameters</span></span>
<span data-ttu-id="b3d76-149">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3d76-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3d76-150">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3d76-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3d76-151">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b3d76-151">INPUTS</span></span>

### <span data-ttu-id="b3d76-152">System.Guid</span><span class="sxs-lookup"><span data-stu-id="b3d76-152">System.Guid</span></span>

### <span data-ttu-id="b3d76-153">System.String</span><span class="sxs-lookup"><span data-stu-id="b3d76-153">System.String</span></span>

## <span data-ttu-id="b3d76-154">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b3d76-154">OUTPUTS</span></span>

### <span data-ttu-id="b3d76-155">Microsoft.Azure.Commands.Automation.Model.Dscnode</span><span class="sxs-lookup"><span data-stu-id="b3d76-155">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="b3d76-156">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b3d76-156">NOTES</span></span>

## <span data-ttu-id="b3d76-157">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b3d76-157">RELATED LINKS</span></span>

[<span data-ttu-id="b3d76-158">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b3d76-158">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="b3d76-159">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b3d76-159">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)

[<span data-ttu-id="b3d76-160">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="b3d76-160">Unregister-AzAutomationDscNode</span></span>](./Unregister-AzAutomationDscNode.md)


