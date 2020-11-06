---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 89C931AE-DA81-47A7-80E4-159C36497DA0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscNodeConfiguration.md
ms.openlocfilehash: f5de98b4f64b4f9adb03493638cdf4e1e613e10f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498006"
---
# <span data-ttu-id="0e1ac-101">Get-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e1ac-101">Get-AzureRmAutomationDscNodeConfiguration</span></span>

## <span data-ttu-id="0e1ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0e1ac-102">SYNOPSIS</span></span>
<span data-ttu-id="0e1ac-103">Ruft Metadaten für DSC-Knoten Konfigurationen in der Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="0e1ac-103">Gets metadata for DSC node configurations in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e1ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e1ac-104">SYNTAX</span></span>

### <span data-ttu-id="0e1ac-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="0e1ac-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration [-RollupStatus <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e1ac-106">ByNodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="0e1ac-106">ByNodeConfigurationName</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration -Name <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e1ac-107">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="0e1ac-107">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscNodeConfiguration -ConfigurationName <String> [-RollupStatus <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0e1ac-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e1ac-108">DESCRIPTION</span></span>
<span data-ttu-id="0e1ac-109">Das Cmdlet " **Get-AzureRmAutomationDscNodeConfiguration** " ruft Metadaten für APS-Knoten Konfigurationen (Desired State Configuration, DSC) in Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="0e1ac-109">The **Get-AzureRmAutomationDscNodeConfiguration** cmdlet gets metadata for APS Desired State Configuration (DSC) node configurations in Azure Automation.</span></span>
<span data-ttu-id="0e1ac-110">Automatisierung speichert die Konfiguration des DSC-Knotens als MOF-Konfigurationsdokument (Managed Object Format).</span><span class="sxs-lookup"><span data-stu-id="0e1ac-110">Automation stores DSC node configuration as a Managed Object Format (MOF) configuration document.</span></span>

## <span data-ttu-id="0e1ac-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0e1ac-111">EXAMPLES</span></span>

### <span data-ttu-id="0e1ac-112">Beispiel 1: Abrufen aller DSC-Knoten Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="0e1ac-112">Example 1: Get all DSC node configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="0e1ac-113">Dieser Befehl ruft Metadaten für alle DSC-Knoten Konfigurationen im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="0e1ac-113">This command gets metadata for all DSC node configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="0e1ac-114">Beispiel 2: Abrufen aller DSC-Knoten Konfigurationen für eine DSC-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="0e1ac-114">Example 2: Get all DSC node configurations for a DSC configuration</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -ConfigurationName "ContosoConfiguration"
```

<span data-ttu-id="0e1ac-115">Dieser Befehl ruft Metadaten für alle DSC-Knoten Konfigurationen im Automatisierungs Konto mit dem Namen Contoso17 ab, die von der DSC-Konfiguration mit dem Namen ContosoConfiguration generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0e1ac-115">This command gets metadata for all DSC node configurations in the Automation account named Contoso17 that the DSC configuration named ContosoConfiguration generated.</span></span>

### <span data-ttu-id="0e1ac-116">Beispiel 3: Abrufen einer DSC-Knoten Konfiguration nach Name</span><span class="sxs-lookup"><span data-stu-id="0e1ac-116">Example 3: Get a DSC node configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscNodeConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration.webserver"
```

<span data-ttu-id="0e1ac-117">Dieser Befehl ruft Metadaten für eine DSC-Knoten Konfiguration mit dem Namen ContosoConfiguration. Webserver im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="0e1ac-117">This command gets metadata for a DSC node configuration with the name ContosoConfiguration.webserver in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="0e1ac-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e1ac-118">PARAMETERS</span></span>

### <span data-ttu-id="0e1ac-119">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0e1ac-119">-AutomationAccountName</span></span>
<span data-ttu-id="0e1ac-120">Gibt den Namen eines Automatisierungs Kontos an, das die DSC-Knoten Konfigurationen enthält, für die dieses Cmdlet Metadaten erhält.</span><span class="sxs-lookup"><span data-stu-id="0e1ac-120">Specifies the name of an Automation account that contains the DSC node configurations for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="0e1ac-121">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="0e1ac-121">-ConfigurationName</span></span>
<span data-ttu-id="0e1ac-122">Gibt den Namen der DSC-Konfiguration an, für die dieses Cmdlet Knoten Konfigurationsmetadaten erhält.</span><span class="sxs-lookup"><span data-stu-id="0e1ac-122">Specifies the name of DSC configuration for which this cmdlet gets node configuration metadata.</span></span>

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

### <span data-ttu-id="0e1ac-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0e1ac-123">-Name</span></span>
<span data-ttu-id="0e1ac-124">Gibt den Namen der DSC-Knoten Konfiguration an, für die dieses Cmdlet Metadaten erhält.</span><span class="sxs-lookup"><span data-stu-id="0e1ac-124">Specifies the name of the DSC node configuration for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="0e1ac-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e1ac-125">-ResourceGroupName</span></span>
<span data-ttu-id="0e1ac-126">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="0e1ac-126">Specifies the name of a resource group.</span></span>
<span data-ttu-id="0e1ac-127">Dieses Cmdlet ruft Metadaten für DSC-Knoten Konfigurationen in der Ressourcengruppe ab, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="0e1ac-127">This cmdlet gets metadata for DSC node configurations in the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="0e1ac-128">-RollupStatus</span><span class="sxs-lookup"><span data-stu-id="0e1ac-128">-RollupStatus</span></span>
<span data-ttu-id="0e1ac-129">Gibt den rollupstatus von DSC-Knoten Konfigurationen an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="0e1ac-129">Specifies the rollup status of DSC node configurations that this cmdlet gets.</span></span>
<span data-ttu-id="0e1ac-130">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="0e1ac-130">Valid values are:</span></span> 

- <span data-ttu-id="0e1ac-131">Schlechte</span><span class="sxs-lookup"><span data-stu-id="0e1ac-131">Bad</span></span> 
- <span data-ttu-id="0e1ac-132">Gute</span><span class="sxs-lookup"><span data-stu-id="0e1ac-132">Good</span></span>

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

### <span data-ttu-id="0e1ac-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e1ac-133">-DefaultProfile</span></span>
<span data-ttu-id="0e1ac-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0e1ac-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e1ac-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e1ac-135">CommonParameters</span></span>
<span data-ttu-id="0e1ac-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e1ac-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e1ac-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e1ac-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e1ac-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0e1ac-138">INPUTS</span></span>

## <span data-ttu-id="0e1ac-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0e1ac-139">OUTPUTS</span></span>

### <span data-ttu-id="0e1ac-140">Microsoft. Azure. Commands. Automation. Model. CompilationJob</span><span class="sxs-lookup"><span data-stu-id="0e1ac-140">Microsoft.Azure.Commands.Automation.Model.CompilationJob</span></span>

## <span data-ttu-id="0e1ac-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="0e1ac-141">NOTES</span></span>

## <span data-ttu-id="0e1ac-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0e1ac-142">RELATED LINKS</span></span>

[<span data-ttu-id="0e1ac-143">Importieren-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="0e1ac-143">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)


