---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73F90276-FABD-414A-B29D-83F371C1ED21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0544b4d5fafcb388b65271e736f43a15f02980c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006574"
---
# <span data-ttu-id="baf10-101">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="baf10-101">Get-AzureAutomationModule</span></span>

## <span data-ttu-id="baf10-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="baf10-102">SYNOPSIS</span></span>

<span data-ttu-id="baf10-103">Rufen Sie ein Azure-Automatisierungs Modul ab.</span><span class="sxs-lookup"><span data-stu-id="baf10-103">Get an Azure Automation module.</span></span>

## <span data-ttu-id="baf10-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="baf10-104">SYNTAX</span></span>

### <span data-ttu-id="baf10-105">Seitensaller (Standard)</span><span class="sxs-lookup"><span data-stu-id="baf10-105">ByAll (Default)</span></span>
```
Get-AzureAutomationModule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="baf10-106">ByName</span><span class="sxs-lookup"><span data-stu-id="baf10-106">ByName</span></span>
```
Get-AzureAutomationModule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="baf10-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="baf10-107">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="baf10-108">Das Cmdlet " **Get-AzureAutomationModule** " ruft mindestens ein Microsoft Azure-Automatisierungs Modul ab.</span><span class="sxs-lookup"><span data-stu-id="baf10-108">The **Get-AzureAutomationModule** cmdlet gets one or more Microsoft Azure Automation modules.</span></span>
<span data-ttu-id="baf10-109">Standardmäßig werden alle Module zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="baf10-109">By default, all modules are returned.</span></span>
<span data-ttu-id="baf10-110">Um ein bestimmtes Modul abzurufen, geben Sie dessen Namen ein.</span><span class="sxs-lookup"><span data-stu-id="baf10-110">To get a specific module, specify its name.</span></span>

## <span data-ttu-id="baf10-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="baf10-111">EXAMPLES</span></span>

### <span data-ttu-id="baf10-112">Beispiel 1: Abrufen aller Module</span><span class="sxs-lookup"><span data-stu-id="baf10-112">Example 1: Get all modules</span></span>
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17"
```

<span data-ttu-id="baf10-113">Dieser Befehl ruft alle Module im Azure Automation-Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="baf10-113">This command gets all modules in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="baf10-114">Beispiel 2: Abrufen eines Moduls</span><span class="sxs-lookup"><span data-stu-id="baf10-114">Example 2: Get a module</span></span>
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

<span data-ttu-id="baf10-115">Dieser Befehl ruft ein Modul mit dem Namen ContosoModule im Azure Automation-Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="baf10-115">This command gets a module named ContosoModule in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="baf10-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="baf10-116">PARAMETERS</span></span>

### <span data-ttu-id="baf10-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="baf10-117">-AutomationAccountName</span></span>
<span data-ttu-id="baf10-118">Gibt den Namen des Automatisierungs Kontos mit dem abzurufenden runbooks an.</span><span class="sxs-lookup"><span data-stu-id="baf10-118">Specifies the name of the Automation account with the runbook to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baf10-119">-Name</span><span class="sxs-lookup"><span data-stu-id="baf10-119">-Name</span></span>
<span data-ttu-id="baf10-120">Gibt den Namen des abzurufenden Moduls an.</span><span class="sxs-lookup"><span data-stu-id="baf10-120">Specifies the name of a module to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baf10-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="baf10-121">-Profile</span></span>
<span data-ttu-id="baf10-122">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="baf10-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="baf10-123">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="baf10-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="baf10-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baf10-124">CommonParameters</span></span>
<span data-ttu-id="baf10-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="baf10-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baf10-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baf10-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baf10-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="baf10-127">INPUTS</span></span>

## <span data-ttu-id="baf10-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="baf10-128">OUTPUTS</span></span>

### <span data-ttu-id="baf10-129">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="baf10-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="baf10-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="baf10-130">NOTES</span></span>

## <span data-ttu-id="baf10-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="baf10-131">RELATED LINKS</span></span>

[<span data-ttu-id="baf10-132">Neu – AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="baf10-132">New-AzureAutomationModule</span></span>](./New-AzureAutomationModule.md)

[<span data-ttu-id="baf10-133">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="baf10-133">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)

[<span data-ttu-id="baf10-134">Satz-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="baf10-134">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


