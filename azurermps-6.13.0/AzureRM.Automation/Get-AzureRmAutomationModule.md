---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
ms.openlocfilehash: 2ed40d0ee0698c8e0ee8d4a1c443db32c843ac65
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662197"
---
# <span data-ttu-id="8018b-101">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8018b-101">Get-AzureRmAutomationModule</span></span>

## <span data-ttu-id="8018b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8018b-102">SYNOPSIS</span></span>
<span data-ttu-id="8018b-103">Ruft Metadaten für Module aus der Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="8018b-103">Gets metadata for modules from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8018b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8018b-104">SYNTAX</span></span>

### <span data-ttu-id="8018b-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="8018b-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8018b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8018b-106">ByName</span></span>
```
Get-AzureRmAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8018b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8018b-107">DESCRIPTION</span></span>
<span data-ttu-id="8018b-108">Das Cmdlet " **Get-AzureRmAutomationModule** " ruft Metadaten für Module aus Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="8018b-108">The **Get-AzureRmAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="8018b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8018b-109">EXAMPLES</span></span>

### <span data-ttu-id="8018b-110">Beispiel 1: Abrufen aller Module</span><span class="sxs-lookup"><span data-stu-id="8018b-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8018b-111">Dieser Befehl ruft alle Module im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="8018b-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="8018b-112">Beispiel 2: Abrufen eines Moduls</span><span class="sxs-lookup"><span data-stu-id="8018b-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8018b-113">Dieser Befehl ruft ein Modul mit dem Namen ContosoModule im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="8018b-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="8018b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8018b-114">PARAMETERS</span></span>

### <span data-ttu-id="8018b-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8018b-115">-AutomationAccountName</span></span>
<span data-ttu-id="8018b-116">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet Modul Metadaten erhält.</span><span class="sxs-lookup"><span data-stu-id="8018b-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="8018b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8018b-117">-DefaultProfile</span></span>
<span data-ttu-id="8018b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8018b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8018b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="8018b-119">-Name</span></span>
<span data-ttu-id="8018b-120">Gibt den Namen des Moduls an, für das dieses Cmdlet Metadaten erhält.</span><span class="sxs-lookup"><span data-stu-id="8018b-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8018b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8018b-121">-ResourceGroupName</span></span>
<span data-ttu-id="8018b-122">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet Modul Metadaten erhält.</span><span class="sxs-lookup"><span data-stu-id="8018b-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="8018b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8018b-123">CommonParameters</span></span>
<span data-ttu-id="8018b-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8018b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8018b-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8018b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8018b-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8018b-126">INPUTS</span></span>

### <span data-ttu-id="8018b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8018b-127">System.String</span></span>

## <span data-ttu-id="8018b-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8018b-128">OUTPUTS</span></span>

### <span data-ttu-id="8018b-129">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="8018b-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="8018b-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="8018b-130">NOTES</span></span>

## <span data-ttu-id="8018b-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8018b-131">RELATED LINKS</span></span>

[<span data-ttu-id="8018b-132">Neu – AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8018b-132">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="8018b-133">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8018b-133">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="8018b-134">Satz-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8018b-134">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


