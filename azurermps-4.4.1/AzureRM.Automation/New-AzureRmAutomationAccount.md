---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2D5B16F0-0662-4D9F-A13F-808CE5EEBBA3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationAccount.md
ms.openlocfilehash: d40e79e53ccf2ddd9cb5c251328268da0bed76fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663090"
---
# <span data-ttu-id="6b862-101">New-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="6b862-101">New-AzureRmAutomationAccount</span></span>

## <span data-ttu-id="6b862-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6b862-102">SYNOPSIS</span></span>
<span data-ttu-id="6b862-103">Erstellt ein Automatisierungs Konto.</span><span class="sxs-lookup"><span data-stu-id="6b862-103">Creates an Automation account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b862-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b862-104">SYNTAX</span></span>

```
New-AzureRmAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Plan <String>] [-Tags <IDictionary>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6b862-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b862-105">DESCRIPTION</span></span>
<span data-ttu-id="6b862-106">Das Cmdlet **New-AzureRmAutomationAccount** erstellt ein Azure Automation-Konto in einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6b862-106">The **New-AzureRmAutomationAccount** cmdlet creates an Azure Automation account in a resource group.</span></span>

<span data-ttu-id="6b862-107">Bei einem Automatisierungs Konto handelt es sich um einen Container für Automatisierungs Ressourcen, der von den Ressourcen anderer Automatisierungs Konten isoliert ist.</span><span class="sxs-lookup"><span data-stu-id="6b862-107">An Automation account is a container for Automation resources that is isolated from the resources of other Automation accounts.</span></span> <span data-ttu-id="6b862-108">Zu den Automatisierungs Ressourcen gehören runbooks, Einstellungen für die gewünschte Zustands Konfiguration (DSC), Aufträge und Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="6b862-108">Automation resources include runbooks, Desired State Configuration (DSC) configurations, jobs, and assets.</span></span>

## <span data-ttu-id="6b862-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b862-109">EXAMPLES</span></span>

### <span data-ttu-id="6b862-110">Beispiel 1: Erstellen eines Automatisierungs Kontos</span><span class="sxs-lookup"><span data-stu-id="6b862-110">Example 1: Create an automation account</span></span>
```
PS C:\> New-AzureRmAutomationAccount -Name "ContosoAutomationAccount" -Location "East US" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6b862-111">Dieser Befehl erstellt ein neues Automatisierungs Konto mit dem Namen ContosoAutomationAccount in der Region Ost-USA.</span><span class="sxs-lookup"><span data-stu-id="6b862-111">This command creates a new automation account named ContosoAutomationAccount in the East US region.</span></span>

## <span data-ttu-id="6b862-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b862-112">PARAMETERS</span></span>

### <span data-ttu-id="6b862-113">-Standort</span><span class="sxs-lookup"><span data-stu-id="6b862-113">-Location</span></span>
<span data-ttu-id="6b862-114">Gibt den Speicherort an, an dem dieses Cmdlet das Automatisierungs Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="6b862-114">Specifies the location in which this cmdlet creates the Automation account.</span></span>
<span data-ttu-id="6b862-115">Verwenden Sie das Get-AzureRMLocation-Cmdlet, um gültige Speicherorte zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="6b862-115">To obtain valid locations, use the Get-AzureRMLocation cmdlet.</span></span>

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

### <span data-ttu-id="6b862-116">-Name</span><span class="sxs-lookup"><span data-stu-id="6b862-116">-Name</span></span>
<span data-ttu-id="6b862-117">Gibt einen Namen für das Automatisierungs Konto an.</span><span class="sxs-lookup"><span data-stu-id="6b862-117">Specifies a name for the Automation account.</span></span>

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

### <span data-ttu-id="6b862-118">-Plan</span><span class="sxs-lookup"><span data-stu-id="6b862-118">-Plan</span></span>
<span data-ttu-id="6b862-119">Gibt den Plan für das Automatisierungs Konto an.</span><span class="sxs-lookup"><span data-stu-id="6b862-119">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="6b862-120">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="6b862-120">Valid values are:</span></span>

- <span data-ttu-id="6b862-121">Grundlegende</span><span class="sxs-lookup"><span data-stu-id="6b862-121">Basic</span></span>
- <span data-ttu-id="6b862-122">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="6b862-122">Free</span></span>

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

### <span data-ttu-id="6b862-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b862-123">-ResourceGroupName</span></span>
<span data-ttu-id="6b862-124">Gibt den Namen einer Ressourcengruppe an, der von diesem Cmdlet ein Automatisierungs Konto hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="6b862-124">Specifies the name of a resource group to which this cmdlet adds an Automation account.</span></span>

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

### <span data-ttu-id="6b862-125">-Tags</span><span class="sxs-lookup"><span data-stu-id="6b862-125">-Tags</span></span>
<span data-ttu-id="6b862-126">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="6b862-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6b862-127">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6b862-127">For example:</span></span>

<span data-ttu-id="6b862-128">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="6b862-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6b862-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b862-129">-DefaultProfile</span></span>
<span data-ttu-id="6b862-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6b862-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b862-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b862-131">CommonParameters</span></span>
<span data-ttu-id="6b862-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b862-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b862-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b862-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b862-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6b862-134">INPUTS</span></span>

## <span data-ttu-id="6b862-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6b862-135">OUTPUTS</span></span>

### <span data-ttu-id="6b862-136">Microsoft. Azure. Commands. Automation. Model. AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="6b862-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="6b862-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="6b862-137">NOTES</span></span>

## <span data-ttu-id="6b862-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6b862-138">RELATED LINKS</span></span>

[<span data-ttu-id="6b862-139">Get-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="6b862-139">Get-AzureRmAutomationAccount</span></span>](./Get-AzureRmAutomationAccount.md)

[<span data-ttu-id="6b862-140">Remove-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="6b862-140">Remove-AzureRmAutomationAccount</span></span>](./Remove-AzureRmAutomationAccount.md)

[<span data-ttu-id="6b862-141">Satz-AzureRmAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="6b862-141">Set-AzureRmAutomationAccount</span></span>](./Set-AzureRmAutomationAccount.md)
