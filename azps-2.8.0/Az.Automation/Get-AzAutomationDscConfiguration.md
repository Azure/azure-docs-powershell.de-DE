---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscConfiguration.md
ms.openlocfilehash: b400efe3224a4fa4b014b9ac93786cd130d4ce6e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658066"
---
# <span data-ttu-id="201fc-101">Get-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="201fc-101">Get-AzAutomationDscConfiguration</span></span>

## <span data-ttu-id="201fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="201fc-102">SYNOPSIS</span></span>
<span data-ttu-id="201fc-103">Ruft DSC-Konfigurationen aus der Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="201fc-103">Gets DSC configurations from Automation.</span></span>

## <span data-ttu-id="201fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="201fc-104">SYNTAX</span></span>

### <span data-ttu-id="201fc-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="201fc-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="201fc-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="201fc-106">ByConfigurationName</span></span>
```
Get-AzAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="201fc-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="201fc-107">DESCRIPTION</span></span>
<span data-ttu-id="201fc-108">Das Cmdlet " **Get-AzAutomationDscConfiguration** " ruft APS-Konfigurationen (Desired State Configuration, DSC) aus Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="201fc-108">The **Get-AzAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="201fc-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="201fc-109">EXAMPLES</span></span>

### <span data-ttu-id="201fc-110">Beispiel 1: Abrufen aller DSC-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="201fc-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="201fc-111">Dieser Befehl ruft Metadaten für alle DSC-Konfigurationen im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="201fc-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="201fc-112">Beispiel 2: Abrufen einer DSC-Konfiguration nach Name</span><span class="sxs-lookup"><span data-stu-id="201fc-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="201fc-113">Dieser Befehl ruft Metadaten für eine DSC-Konfiguration mit dem Namen myconfiguration im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="201fc-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="201fc-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="201fc-114">PARAMETERS</span></span>

### <span data-ttu-id="201fc-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="201fc-115">-AutomationAccountName</span></span>
<span data-ttu-id="201fc-116">Gibt den Namen des Automatisierungs Kontos an, das DSC-Konfigurationen enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="201fc-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="201fc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="201fc-117">-DefaultProfile</span></span>
<span data-ttu-id="201fc-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="201fc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="201fc-119">-Name</span><span class="sxs-lookup"><span data-stu-id="201fc-119">-Name</span></span>
<span data-ttu-id="201fc-120">Gibt den Namen der DSC-Konfiguration an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="201fc-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: ByConfigurationName
Aliases: ConfigurationName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="201fc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="201fc-121">-ResourceGroupName</span></span>
<span data-ttu-id="201fc-122">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet DSC-Konfigurationen erhält.</span><span class="sxs-lookup"><span data-stu-id="201fc-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="201fc-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="201fc-123">CommonParameters</span></span>
<span data-ttu-id="201fc-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="201fc-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="201fc-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="201fc-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="201fc-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="201fc-126">INPUTS</span></span>

### <span data-ttu-id="201fc-127">System. String</span><span class="sxs-lookup"><span data-stu-id="201fc-127">System.String</span></span>

## <span data-ttu-id="201fc-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="201fc-128">OUTPUTS</span></span>

### <span data-ttu-id="201fc-129">Microsoft. Azure. Commands. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="201fc-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="201fc-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="201fc-130">NOTES</span></span>

## <span data-ttu-id="201fc-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="201fc-131">RELATED LINKS</span></span>

[<span data-ttu-id="201fc-132">Export-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="201fc-132">Export-AzAutomationDscConfiguration</span></span>](./Export-AzAutomationDscConfiguration.md)

[<span data-ttu-id="201fc-133">Importieren-AzAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="201fc-133">Import-AzAutomationDscConfiguration</span></span>](./Import-AzAutomationDscConfiguration.md)


