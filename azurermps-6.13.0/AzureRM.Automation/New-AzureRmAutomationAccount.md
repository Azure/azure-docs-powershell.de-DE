---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: 2d7c038f9f226f074bfe534df40471959607f3d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476289"
---
# <span data-ttu-id="1501c-101">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1501c-101">New-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="1501c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1501c-102">SYNOPSIS</span></span>
<span data-ttu-id="1501c-103">Erstellt ein Automatisierungs Konto.</span><span class="sxs-lookup"><span data-stu-id="1501c-103">Creates an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1501c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1501c-104">SYNTAX</span></span>

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1501c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1501c-105">DESCRIPTION</span></span>
<span data-ttu-id="1501c-106">Das Cmdlet **New-AzureRmAutomationAccount** erstellt ein Azure Automation-Konto in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1501c-106">The **New-AzureRmAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>
<span data-ttu-id="1501c-107">Bei einem Automatisierungs Konto handelt es sich um einen Container für Automatisierungs Ressourcen, der von den Ressourcen anderer Automatisierungs Konten isoliert ist.</span><span class="sxs-lookup"><span data-stu-id="1501c-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="1501c-108">Zu den Automatisierungs Ressourcen gehören runbooks, Einstellungen für die gewünschte Zustands Konfiguration (DSC), Aufträge und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="1501c-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="1501c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1501c-109">EXAMPLES</span></span>

### <span data-ttu-id="1501c-110">Beispiel 1: Erstellen eines Automatisierungs Kontos</span><span class="sxs-lookup"><span data-stu-id="1501c-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1501c-111">Dieser Befehl erstellt ein neues Automatisierungs Konto mit dem Namen ContosoAutomationAccount in der Region Ost-USA.</span><span class="sxs-lookup"><span data-stu-id="1501c-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="1501c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1501c-112">PARAMETERS</span></span>

### <span data-ttu-id="1501c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1501c-113">-DefaultProfile</span></span>
<span data-ttu-id="1501c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1501c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1501c-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="1501c-115">-Location</span></span>
<span data-ttu-id="1501c-116">Gibt den Speicherort an, an dem dieses Cmdlet das Automatisierungs Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="1501c-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="1501c-117">Verwenden Sie das Get-AzureRMLocation-Cmdlet, um gültige Speicherorte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1501c-117">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1501c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1501c-118">-Name</span></span>
<span data-ttu-id="1501c-119">Gibt einen Namen für das Automatisierungs Konto an.</span><span class="sxs-lookup"><span data-stu-id="1501c-119">Specifies a name for the Automation account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1501c-120">-Plan</span><span class="sxs-lookup"><span data-stu-id="1501c-120">-Plan</span></span>
<span data-ttu-id="1501c-121">Gibt den Plan für das Automatisierungs Konto an.</span><span class="sxs-lookup"><span data-stu-id="1501c-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="1501c-122">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="1501c-122">Valid values are:</span></span>
- <span data-ttu-id="1501c-123">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="1501c-123">Basic</span></span>
- <span data-ttu-id="1501c-124">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="1501c-124">Free</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1501c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1501c-125">-ResourceGroupName</span></span>
<span data-ttu-id="1501c-126">Gibt den Namen einer Ressourcengruppe an, der von diesem Cmdlet ein Automatisierungs Konto hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="1501c-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="1501c-127">-Tags</span><span class="sxs-lookup"><span data-stu-id="1501c-127">-Tags</span></span>
<span data-ttu-id="1501c-128">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="1501c-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1501c-129">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="1501c-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1501c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1501c-130">CommonParameters</span></span>
<span data-ttu-id="1501c-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1501c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1501c-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1501c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1501c-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1501c-133">INPUTS</span></span>

### <span data-ttu-id="1501c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1501c-134">System.String</span></span>

### <span data-ttu-id="1501c-135">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="1501c-135">System.Collections.IDictionary</span></span>

## <span data-ttu-id="1501c-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1501c-136">OUTPUTS</span></span>

### <span data-ttu-id="1501c-137">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1501c-137">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="1501c-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="1501c-138">NOTES</span></span>

## <span data-ttu-id="1501c-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1501c-139">RELATED LINKS</span></span>

[<span data-ttu-id="1501c-140">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1501c-140">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="1501c-141">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1501c-141">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="1501c-142">Satz-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="1501c-142">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)
