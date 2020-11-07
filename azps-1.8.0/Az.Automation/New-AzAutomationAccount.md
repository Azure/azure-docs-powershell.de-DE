---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationAccount.md
ms.openlocfilehash: 4486301d6a7e39081e297d018f3aa244459d328b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661781"
---
# <span data-ttu-id="58ce3-101">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="58ce3-101">New-AzAutomationAccount</span></span>

## <span data-ttu-id="58ce3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="58ce3-102">SYNOPSIS</span></span>
<span data-ttu-id="58ce3-103">Erstellt ein Automatisierungs Konto.</span><span class="sxs-lookup"><span data-stu-id="58ce3-103">Creates an Automation account.</span></span>

## <span data-ttu-id="58ce3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="58ce3-104">SYNTAX</span></span>

```
New-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Plan <String>]
 [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58ce3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="58ce3-105">DESCRIPTION</span></span>
<span data-ttu-id="58ce3-106">Das Cmdlet **New-AzAutomationAccount** erstellt ein Azure Automation-Konto in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="58ce3-106">The **New-AzAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>
<span data-ttu-id="58ce3-107">Bei einem Automatisierungs Konto handelt es sich um einen Container für Automatisierungs Ressourcen, der von den Ressourcen anderer Automatisierungs Konten isoliert ist.</span><span class="sxs-lookup"><span data-stu-id="58ce3-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="58ce3-108">Zu den Automatisierungs Ressourcen gehören runbooks, Einstellungen für die gewünschte Zustands Konfiguration (DSC), Aufträge und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="58ce3-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="58ce3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="58ce3-109">EXAMPLES</span></span>

### <span data-ttu-id="58ce3-110">Beispiel 1: Erstellen eines Automatisierungs Kontos</span><span class="sxs-lookup"><span data-stu-id="58ce3-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="58ce3-111">Dieser Befehl erstellt ein neues Automatisierungs Konto mit dem Namen ContosoAutomationAccount in der Region Ost-USA.</span><span class="sxs-lookup"><span data-stu-id="58ce3-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="58ce3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="58ce3-112">PARAMETERS</span></span>

### <span data-ttu-id="58ce3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58ce3-113">-DefaultProfile</span></span>
<span data-ttu-id="58ce3-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="58ce3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58ce3-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="58ce3-115">-Location</span></span>
<span data-ttu-id="58ce3-116">Gibt den Speicherort an, an dem dieses Cmdlet das Automatisierungs Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="58ce3-116">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="58ce3-117">Verwenden Sie das Get-AzLocation-Cmdlet, um gültige Speicherorte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="58ce3-117">To obtain valid locations, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="58ce3-118">-Name</span><span class="sxs-lookup"><span data-stu-id="58ce3-118">-Name</span></span>
<span data-ttu-id="58ce3-119">Gibt einen Namen für das Automatisierungs Konto an.</span><span class="sxs-lookup"><span data-stu-id="58ce3-119">Specifies a name for the Automation account.</span></span>

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

### <span data-ttu-id="58ce3-120">-Plan</span><span class="sxs-lookup"><span data-stu-id="58ce3-120">-Plan</span></span>
<span data-ttu-id="58ce3-121">Gibt den Plan für das Automatisierungs Konto an.</span><span class="sxs-lookup"><span data-stu-id="58ce3-121">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="58ce3-122">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="58ce3-122">Valid values are:</span></span>
- <span data-ttu-id="58ce3-123">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="58ce3-123">Basic</span></span>
- <span data-ttu-id="58ce3-124">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="58ce3-124">Free</span></span>

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

### <span data-ttu-id="58ce3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58ce3-125">-ResourceGroupName</span></span>
<span data-ttu-id="58ce3-126">Gibt den Namen einer Ressourcengruppe an, der von diesem Cmdlet ein Automatisierungs Konto hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="58ce3-126">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="58ce3-127">-Tags</span><span class="sxs-lookup"><span data-stu-id="58ce3-127">-Tags</span></span>
<span data-ttu-id="58ce3-128">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="58ce3-128">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="58ce3-129">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="58ce3-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="58ce3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ce3-130">CommonParameters</span></span>
<span data-ttu-id="58ce3-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58ce3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ce3-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58ce3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ce3-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="58ce3-133">INPUTS</span></span>

### <span data-ttu-id="58ce3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="58ce3-134">System.String</span></span>

### <span data-ttu-id="58ce3-135">System. Collections. IDictionary</span><span class="sxs-lookup"><span data-stu-id="58ce3-135">System.Collections.IDictionary</span></span>

## <span data-ttu-id="58ce3-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="58ce3-136">OUTPUTS</span></span>

### <span data-ttu-id="58ce3-137">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="58ce3-137">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="58ce3-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="58ce3-138">NOTES</span></span>

## <span data-ttu-id="58ce3-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="58ce3-139">RELATED LINKS</span></span>

[<span data-ttu-id="58ce3-140">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="58ce3-140">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="58ce3-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="58ce3-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)

[<span data-ttu-id="58ce3-142">Satz-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="58ce3-142">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)
