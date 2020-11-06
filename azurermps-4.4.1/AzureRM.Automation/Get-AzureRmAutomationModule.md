---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRmAutomationModule.md
ms.openlocfilehash: dcd84c47ff9a6dae06daaf05bde6dd6f4af86553
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497978"
---
# <span data-ttu-id="7743b-101">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7743b-101">Get-AzureRmAutomationModule</span></span>

## <span data-ttu-id="7743b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7743b-102">SYNOPSIS</span></span>
<span data-ttu-id="7743b-103">Ruft Metadaten für Module aus der Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="7743b-103">Gets metadata for modules from Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7743b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7743b-104">SYNTAX</span></span>

### <span data-ttu-id="7743b-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="7743b-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7743b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="7743b-106">ByName</span></span>
```
Get-AzureRmAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7743b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7743b-107">DESCRIPTION</span></span>
<span data-ttu-id="7743b-108">Das Cmdlet " **Get-AzureRmAutomationModule** " ruft Metadaten für Module aus Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="7743b-108">The **Get-AzureRmAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="7743b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7743b-109">EXAMPLES</span></span>

### <span data-ttu-id="7743b-110">Beispiel 1: Abrufen aller Module</span><span class="sxs-lookup"><span data-stu-id="7743b-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7743b-111">Dieser Befehl ruft alle Module im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="7743b-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="7743b-112">Beispiel 2: Abrufen eines Moduls</span><span class="sxs-lookup"><span data-stu-id="7743b-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7743b-113">Dieser Befehl ruft ein Modul mit dem Namen ContosoModule im Automatisierungs Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="7743b-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="7743b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7743b-114">PARAMETERS</span></span>

### <span data-ttu-id="7743b-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7743b-115">-AutomationAccountName</span></span>
<span data-ttu-id="7743b-116">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet Modul Metadaten erhält.</span><span class="sxs-lookup"><span data-stu-id="7743b-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="7743b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7743b-117">-Name</span></span>
<span data-ttu-id="7743b-118">Gibt den Namen des Moduls an, für das dieses Cmdlet Metadaten erhält.</span><span class="sxs-lookup"><span data-stu-id="7743b-118">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

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

### <span data-ttu-id="7743b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7743b-119">-ResourceGroupName</span></span>
<span data-ttu-id="7743b-120">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet Modul Metadaten erhält.</span><span class="sxs-lookup"><span data-stu-id="7743b-120">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="7743b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7743b-121">-DefaultProfile</span></span>
<span data-ttu-id="7743b-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7743b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7743b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7743b-123">CommonParameters</span></span>
<span data-ttu-id="7743b-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7743b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7743b-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7743b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7743b-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7743b-126">INPUTS</span></span>

## <span data-ttu-id="7743b-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7743b-127">OUTPUTS</span></span>

### <span data-ttu-id="7743b-128">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="7743b-128">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="7743b-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="7743b-129">NOTES</span></span>

## <span data-ttu-id="7743b-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7743b-130">RELATED LINKS</span></span>

[<span data-ttu-id="7743b-131">Neu – AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7743b-131">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="7743b-132">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7743b-132">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="7743b-133">Satz-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="7743b-133">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


