---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: b139ed5b67bbc36bad45ab2528ed74299d40c1b9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927472"
---
# <span data-ttu-id="8e9ef-101">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e9ef-101">Get-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="8e9ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e9ef-102">SYNOPSIS</span></span>
<span data-ttu-id="8e9ef-103">Ruft Metadaten für DSC-Knotenkonfigurationen in der Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-103">Gets metadata for DSC node configurations in Automation.</span></span>

## <span data-ttu-id="8e9ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e9ef-104">SYNTAX</span></span>

### <span data-ttu-id="8e9ef-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e9ef-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e9ef-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8e9ef-106">ByNodeConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e9ef-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8e9ef-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e9ef-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e9ef-108">DESCRIPTION</span></span>
<span data-ttu-id="8e9ef-109">Das **Cmdlet Get-AzAutomationDscNodeConfiguration** ruft Metadaten für APS Desired State Configuration (DSC)-Knotenkonfigurationen in Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-109">The **Get-AzAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="8e9ef-110">Bei der Automatisierung wird die KONFIGURATION von DSC-Knoten als MoF(Managed Object Format)-Konfigurationsdokument gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="8e9ef-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e9ef-111">EXAMPLES</span></span>

### <span data-ttu-id="8e9ef-112">Beispiel 1: Alle DSC-Knotenkonfigurationen erhalten</span><span class="sxs-lookup"><span data-stu-id="8e9ef-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="8e9ef-113">Dieser Befehl ruft Metadaten für alle DSC-Knotenkonfigurationen im Automatisierungskonto namens Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="8e9ef-114">Beispiel 2: Alle DSC-Knotenkonfigurationen für eine DSC-Konfiguration erhalten</span><span class="sxs-lookup"><span data-stu-id="8e9ef-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="8e9ef-115">Dieser Befehl ruft Metadaten für alle DSC-Knotenkonfigurationen im Automatisierungskonto namens Contoso17 ab, das von der DSC-Konfiguration namens ContosoConfiguration generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="8e9ef-116">Beispiel 3: Benennen einer KONFIGURATION eines DSC-Knotens</span><span class="sxs-lookup"><span data-stu-id="8e9ef-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="8e9ef-117">Dieser Befehl ruft Metadaten für eine DSC-Knotenkonfiguration mit dem Namen ContosoConfiguration.webserver im Automatisierungskonto namens Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="8e9ef-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8e9ef-118">PARAMETERS</span></span>

### <span data-ttu-id="8e9ef-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8e9ef-119">-AutomationAccountName</span></span>
<span data-ttu-id="8e9ef-120">Gibt den Namen eines Automatisierungskontos an, das die DSC-Knotenkonfigurationen enthält, für die dieses Cmdlet Metadaten erhält.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="8e9ef-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8e9ef-121">-ConfigurationName</span></span>
<span data-ttu-id="8e9ef-122">Gibt den Namen der DSC-Konfiguration an, für die dieses Cmdlet Knotenkonfigurationsmetadaten erhält.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e9ef-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e9ef-123">-DefaultProfile</span></span>
<span data-ttu-id="8e9ef-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8e9ef-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e9ef-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8e9ef-125">-Name</span></span>
<span data-ttu-id="8e9ef-126">Gibt den Namen der KONFIGURATION des DSC-Knotens an, für die dieses Cmdlet Metadaten erhält.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-126">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByNodeConfigurationName
Aliases: NodeConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e9ef-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e9ef-127">-ResourceGroupName</span></span>
<span data-ttu-id="8e9ef-128">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-128">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8e9ef-129">Dieses Cmdlet ruft Metadaten für DSC-Knotenkonfigurationen in der Ressourcengruppe ab, die von diesem Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-129">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8e9ef-130">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="8e9ef-130">-RollupStatus</span></span>
<span data-ttu-id="8e9ef-131">Gibt den Rollupstatus von DSC-Knotenkonfigurationen an, die von diesem Cmdlet abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-131">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="8e9ef-132">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="8e9ef-132">Valid values are:</span></span> 
- <span data-ttu-id="8e9ef-133">Schlecht</span><span class="sxs-lookup"><span data-stu-id="8e9ef-133">Bad</span></span> 
- <span data-ttu-id="8e9ef-134">Gut</span><span class="sxs-lookup"><span data-stu-id="8e9ef-134">Good</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, ByConfigurationName
Aliases:
Accepted values: Good, Bad

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e9ef-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e9ef-135">CommonParameters</span></span>
<span data-ttu-id="8e9ef-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e9ef-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e9ef-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e9ef-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e9ef-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e9ef-138">INPUTS</span></span>

### <span data-ttu-id="8e9ef-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8e9ef-139">System.String</span></span>

## <span data-ttu-id="8e9ef-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e9ef-140">OUTPUTS</span></span>

### <span data-ttu-id="8e9ef-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span><span class="sxs-lookup"><span data-stu-id="8e9ef-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="8e9ef-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8e9ef-142">NOTES</span></span>

## <span data-ttu-id="8e9ef-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8e9ef-143">RELATED LINKS</span></span>

[<span data-ttu-id="8e9ef-144">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e9ef-144">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)


