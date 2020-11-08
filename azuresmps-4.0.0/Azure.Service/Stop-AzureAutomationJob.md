---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 2E363D6B-7A05-4C54-B005-68FDBA49A105
online version: ''
schema: 2.0.0
ms.openlocfilehash: cda64b916635d3b46ffb7e8b4170330810a95b5b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006148"
---
# <span data-ttu-id="047e3-101">Stop-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="047e3-101">Stop-AzureAutomationJob</span></span>

## <span data-ttu-id="047e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="047e3-102">SYNOPSIS</span></span>

<span data-ttu-id="047e3-103">Beendet einen Automatisierungs Auftrag.</span><span class="sxs-lookup"><span data-stu-id="047e3-103">Stops an Automation job.</span></span>

## <span data-ttu-id="047e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="047e3-104">SYNTAX</span></span>

```
Stop-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="047e3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="047e3-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="047e3-106">Das Cmdlet **Stop-AzureAutomationJob** beendet einen Microsoft Azure-Automatisierungs Auftrag.</span><span class="sxs-lookup"><span data-stu-id="047e3-106">The **Stop-AzureAutomationJob** cmdlet stops a Microsoft Azure Automation job.</span></span>
<span data-ttu-id="047e3-107">Geben Sie einen ausgeführten Automatisierungs Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="047e3-107">Specify a running automation job.</span></span>

## <span data-ttu-id="047e3-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="047e3-108">EXAMPLES</span></span>

### <span data-ttu-id="047e3-109">Beispiel 1: Beenden eines Auftrags</span><span class="sxs-lookup"><span data-stu-id="047e3-109">Example 1: Stop a job</span></span>
```
PS C:\> Stop-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="047e3-110">Mit diesem Befehl wird der Auftrag beendet, der die angegebene ID aufweist.</span><span class="sxs-lookup"><span data-stu-id="047e3-110">This command stops the job that has the specified ID.</span></span>

## <span data-ttu-id="047e3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="047e3-111">PARAMETERS</span></span>

### <span data-ttu-id="047e3-112">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="047e3-112">-AutomationAccountName</span></span>
<span data-ttu-id="047e3-113">Gibt den Namen eines Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="047e3-113">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="047e3-114">-ID</span><span class="sxs-lookup"><span data-stu-id="047e3-114">-Id</span></span>
<span data-ttu-id="047e3-115">Gibt die ID eines Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="047e3-115">Specifies the ID of a job.</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: JobId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="047e3-116">-Profil</span><span class="sxs-lookup"><span data-stu-id="047e3-116">-Profile</span></span>
<span data-ttu-id="047e3-117">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="047e3-117">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="047e3-118">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="047e3-118">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="047e3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="047e3-119">CommonParameters</span></span>
<span data-ttu-id="047e3-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="047e3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="047e3-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="047e3-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="047e3-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="047e3-122">INPUTS</span></span>

## <span data-ttu-id="047e3-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="047e3-123">OUTPUTS</span></span>

## <span data-ttu-id="047e3-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="047e3-124">NOTES</span></span>

## <span data-ttu-id="047e3-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="047e3-125">RELATED LINKS</span></span>

[<span data-ttu-id="047e3-126">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="047e3-126">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="047e3-127">Lebenslauf-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="047e3-127">Resume-AzureAutomationJob</span></span>](./Resume-AzureAutomationJob.md)

[<span data-ttu-id="047e3-128">Suspend-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="047e3-128">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


