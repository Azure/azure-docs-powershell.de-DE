---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfiguration.md
ms.openlocfilehash: 1114d0a78518c33126f28fb4b409a881a52a4ae7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997403"
---
# <span data-ttu-id="8e1de-101">Get-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e1de-101">Get-AzAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="8e1de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8e1de-102">SYNOPSIS</span></span>
<span data-ttu-id="8e1de-103">Ruft Metadaten für DSC-Knoten Konfigurationen in der Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="8e1de-103">Gets metadata for DSC node configurations in Automation.</span></span>

## <span data-ttu-id="8e1de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8e1de-104">SYNTAX</span></span>

### <span data-ttu-id="8e1de-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="8e1de-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e1de-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8e1de-106">ByNodeConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8e1de-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8e1de-107">ByConfigurationName</span></span>
```
Get-AzAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8e1de-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8e1de-108">DESCRIPTION</span></span>
<span data-ttu-id="8e1de-109">Das Cmdlet " **Get-AzAutomationDscNodeConfiguration** " ruft Metadaten für APS-Knoten Konfigurationen (Desired State Configuration, DSC) in Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="8e1de-109">The **Get-AzAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="8e1de-110">Automatisierung speichert die Konfiguration des DSC-Knotens als MOF-Konfigurationsdokument (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="8e1de-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="8e1de-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8e1de-111">EXAMPLES</span></span>

### <span data-ttu-id="8e1de-112">Beispiel 1: Abrufen aller DSC-Knoten Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="8e1de-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="8e1de-113">Dieser Befehl ruft Metadaten für alle DSC-Knoten Konfigurationen im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="8e1de-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="8e1de-114">Beispiel 2: Abrufen aller DSC-Knoten Konfigurationen für eine DSC-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="8e1de-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="8e1de-115">Dieser Befehl ruft Metadaten für alle DSC-Knoten Konfigurationen im Automatisierungs Konto mit dem Namen Contoso17 ab, die von der DSC-Konfiguration mit dem Namen ContosoConfiguration generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="8e1de-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="8e1de-116">Beispiel 3: Abrufen einer DSC-Knoten Konfiguration nach Name</span><span class="sxs-lookup"><span data-stu-id="8e1de-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="8e1de-117">Dieser Befehl ruft Metadaten für eine DSC-Knoten Konfiguration mit dem Namen ContosoConfiguration. Webserver im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="8e1de-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="8e1de-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="8e1de-118">PARAMETERS</span></span>

### <span data-ttu-id="8e1de-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8e1de-119">-AutomationAccountName</span></span>
<span data-ttu-id="8e1de-120">Gibt den Namen eines Automatisierungs Kontos an, das die DSC-Knoten Konfigurationen enthält, für die dieses Cmdlet Metadaten erhält.</span><span class="sxs-lookup"><span data-stu-id="8e1de-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="8e1de-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8e1de-121">-ConfigurationName</span></span>
<span data-ttu-id="8e1de-122">Gibt den Namen der DSC-Konfiguration an, für die dieses Cmdlet Knoten Konfigurationsmetadaten erhält.</span><span class="sxs-lookup"><span data-stu-id="8e1de-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

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

### <span data-ttu-id="8e1de-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e1de-123">-DefaultProfile</span></span>
<span data-ttu-id="8e1de-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8e1de-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e1de-125">-Name</span><span class="sxs-lookup"><span data-stu-id="8e1de-125">-Name</span></span>
<span data-ttu-id="8e1de-126">Gibt den Namen der DSC-Knoten Konfiguration an, für die dieses Cmdlet Metadaten erhält.</span><span class="sxs-lookup"><span data-stu-id="8e1de-126">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="8e1de-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e1de-127">-ResourceGroupName</span></span>
<span data-ttu-id="8e1de-128">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="8e1de-128">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8e1de-129">Dieses Cmdlet ruft Metadaten für DSC-Knoten Konfigurationen in der Ressourcengruppe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="8e1de-129">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="8e1de-130">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="8e1de-130">-RollupStatus</span></span>
<span data-ttu-id="8e1de-131">Gibt den rollupstatus von DSC-Knoten Konfigurationen an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="8e1de-131">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="8e1de-132">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="8e1de-132">Valid values are:</span></span> 
- <span data-ttu-id="8e1de-133">Schlechte</span><span class="sxs-lookup"><span data-stu-id="8e1de-133">Bad</span></span> 
- <span data-ttu-id="8e1de-134">Gute</span><span class="sxs-lookup"><span data-stu-id="8e1de-134">Good</span></span>

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

### <span data-ttu-id="8e1de-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e1de-135">CommonParameters</span></span>
<span data-ttu-id="8e1de-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e1de-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e1de-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e1de-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e1de-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8e1de-138">INPUTS</span></span>

### <span data-ttu-id="8e1de-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8e1de-139">System.String</span></span>

## <span data-ttu-id="8e1de-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8e1de-140">OUTPUTS</span></span>

### <span data-ttu-id="8e1de-141">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="8e1de-141">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="8e1de-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="8e1de-142">NOTES</span></span>

## <span data-ttu-id="8e1de-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8e1de-143">RELATED LINKS</span></span>

[<span data-ttu-id="8e1de-144">Importieren-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="8e1de-144">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)


