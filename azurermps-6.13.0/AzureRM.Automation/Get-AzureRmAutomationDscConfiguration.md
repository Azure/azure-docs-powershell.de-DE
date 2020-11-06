---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: BBD37C4B-BB6F-4560-BDEE-F0440EC1938A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationDscConfiguration.md
ms.openlocfilehash: 10e04dc24c34ba60186c8166e2626524fcc60a37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476302"
---
# <span data-ttu-id="9d34c-101">Get-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d34c-101">Get-AzureRmAutomationDscConfiguration</span></span>

## <span data-ttu-id="9d34c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d34c-102">SYNOPSIS</span></span>
<span data-ttu-id="9d34c-103">Ruft DSC-Konfigurationen aus der Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="9d34c-103">Gets DSC configurations from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d34c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d34c-104">SYNTAX</span></span>

### <span data-ttu-id="9d34c-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="9d34c-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationDscConfiguration [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9d34c-106">ByConfigurationName</span><span class="sxs-lookup"><span data-stu-id="9d34c-106">ByConfigurationName</span></span>
```
Get-AzureRmAutomationDscConfiguration [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d34c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d34c-107">DESCRIPTION</span></span>
<span data-ttu-id="9d34c-108">Das Cmdlet " **Get-AzureRmAutomationDscConfiguration** " ruft APS-Konfigurationen (Desired State Configuration, DSC) aus Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="9d34c-108">The **Get-AzureRmAutomationDscConfiguration** cmdlet gets APS Desired State Configuration (DSC) configurations from Azure Automation.</span></span>

## <span data-ttu-id="9d34c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d34c-109">EXAMPLES</span></span>

### <span data-ttu-id="9d34c-110">Beispiel 1: Abrufen aller DSC-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="9d34c-110">Example 1: Get all DSC configurations</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="9d34c-111">Dieser Befehl ruft Metadaten für alle DSC-Konfigurationen im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="9d34c-111">This command gets metadata for all DSC configurations in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="9d34c-112">Beispiel 2: Abrufen einer DSC-Konfiguration nach Name</span><span class="sxs-lookup"><span data-stu-id="9d34c-112">Example 2: Get a DSC configuration by name</span></span>
```
PS C:\>Get-AzureRmAutomationDscConfiguration -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "ContosoConfiguration"
```

<span data-ttu-id="9d34c-113">Dieser Befehl ruft Metadaten für eine DSC-Konfiguration mit dem Namen myconfiguration im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="9d34c-113">This command gets metadata for a DSC configuration named MyConfiguration in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="9d34c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d34c-114">PARAMETERS</span></span>

### <span data-ttu-id="9d34c-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="9d34c-115">-AutomationAccountName</span></span>
<span data-ttu-id="9d34c-116">Gibt den Namen des Automatisierungs Kontos an, das DSC-Konfigurationen enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="9d34c-116">Specifies the name of the Automation account that contains DSC configurations that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9d34c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d34c-117">-DefaultProfile</span></span>
<span data-ttu-id="9d34c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9d34c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d34c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9d34c-119">-Name</span></span>
<span data-ttu-id="9d34c-120">Gibt den Namen der DSC-Konfiguration an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="9d34c-120">Specifies the name of the DSC configuration that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9d34c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d34c-121">-ResourceGroupName</span></span>
<span data-ttu-id="9d34c-122">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet DSC-Konfigurationen erhält.</span><span class="sxs-lookup"><span data-stu-id="9d34c-122">Specifies the name of a resource group for which this cmdlet gets DSC configurations.</span></span>

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

### <span data-ttu-id="9d34c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d34c-123">CommonParameters</span></span>
<span data-ttu-id="9d34c-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d34c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d34c-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d34c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d34c-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d34c-126">INPUTS</span></span>

### <span data-ttu-id="9d34c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="9d34c-127">System.String</span></span>

## <span data-ttu-id="9d34c-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d34c-128">OUTPUTS</span></span>

### <span data-ttu-id="9d34c-129">Microsoft. Azure. Commands. Automation. Model. DscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d34c-129">Microsoft.Azure.Commands.Automation.Model.DscConfiguration</span></span>

## <span data-ttu-id="9d34c-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d34c-130">NOTES</span></span>

## <span data-ttu-id="9d34c-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d34c-131">RELATED LINKS</span></span>

[<span data-ttu-id="9d34c-132">Export-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d34c-132">Export-AzureRmAutomationDscConfiguration</span></span>](./Export-AzureRmAutomationDscConfiguration.md)

[<span data-ttu-id="9d34c-133">Importieren-AzureRmAutomationDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="9d34c-133">Import-AzureRmAutomationDscConfiguration</span></span>](./Import-AzureRmAutomationDscConfiguration.md)


