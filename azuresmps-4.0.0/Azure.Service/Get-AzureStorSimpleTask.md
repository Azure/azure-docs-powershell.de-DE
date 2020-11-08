---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: CF3548F6-03FE-44D6-AA2C-1015611C657A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0423fe51a047385ef6395075dd116b4d4189c667
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005758"
---
# <span data-ttu-id="c82e5-101">Get-AzureStorSimpleTask</span><span class="sxs-lookup"><span data-stu-id="c82e5-101">Get-AzureStorSimpleTask</span></span>

## <span data-ttu-id="c82e5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c82e5-102">SYNOPSIS</span></span>
<span data-ttu-id="c82e5-103">Ruft den Status einer Aufgabe auf einem StorSimple-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="c82e5-103">Gets status of a task on a StorSimple device.</span></span>

## <span data-ttu-id="c82e5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c82e5-104">SYNTAX</span></span>

```
Get-AzureStorSimpleTask -InstanceId <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="c82e5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c82e5-105">DESCRIPTION</span></span>
<span data-ttu-id="c82e5-106">Das Cmdlet " **Get-AzureStorSimpleTask** " Ruft den Status einer Aufgabe ab, die auf einem Azure StorSimple-Gerät asynchron ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c82e5-106">The **Get-AzureStorSimpleTask** cmdlet retrieves the status of a task that runs asynchronously on an Azure StorSimple device.</span></span>

<span data-ttu-id="c82e5-107">Beim Verwalten eines StorSimple-Geräts können die meisten Aktionen zum Erstellen, lesen, aktualisieren und löschen asynchron ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c82e5-107">While you manage a StorSimple device, most create, read, update, and delete actions can run asynchronously.</span></span>
<span data-ttu-id="c82e5-108">Windows PowerShell gibt eine **Aufgaben** -Nr zurück.</span><span class="sxs-lookup"><span data-stu-id="c82e5-108">Windows PowerShell returns a **TaskId**.</span></span>
<span data-ttu-id="c82e5-109">Verwenden Sie die ID, um den aktuellen Status der Aufgabe abzurufen.</span><span class="sxs-lookup"><span data-stu-id="c82e5-109">Use the ID to get the current status of the task.</span></span>

## <span data-ttu-id="c82e5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c82e5-110">EXAMPLES</span></span>

### <span data-ttu-id="c82e5-111">Beispiel 1: Abrufen des Status einer Aufgabe</span><span class="sxs-lookup"><span data-stu-id="c82e5-111">Example 1: Get the status of a task</span></span>
```
PS C:\>Get-AzureStorSimpleTask -TaskId "53816d8d-a8b5-4c1d-a177-e59007608d6d"
VERBOSE: ClientRequestId: d9c1e8a7-994f-4698-8b42-064600b45cad_PS
VERBOSE: ClientRequestId: aae17c82-6fd3-435e-a965-1c66b3c955fe_PS


AsyncTaskAggregatedResult : Succeeded
Error                     : Microsoft.WindowsAzure.Management.StorSimple.Models.ErrorDetails
Result                    : Succeeded
Status                    : Completed
TaskId                    : 53816d8d-a8b5-4c1d-a177-e59007608d6d
TaskSteps                 : {}
StatusCode                : OK
RequestId                 : e9174990825750bba69383748f23019c
```

<span data-ttu-id="c82e5-112">Dieser Befehl ruft den Status der Aufgabe ab, die die angegebene ID aufweist.</span><span class="sxs-lookup"><span data-stu-id="c82e5-112">This command gets the status of the task that has the specified ID.</span></span>
<span data-ttu-id="c82e5-113">Die Ergebnisse zeigen, dass der Vorgang den Status abgeschlossen und das Ergebnis erfolgreich aufweist.</span><span class="sxs-lookup"><span data-stu-id="c82e5-113">The results show that the task has a status of completed and a result of successful.</span></span>

## <span data-ttu-id="c82e5-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c82e5-114">PARAMETERS</span></span>

### <span data-ttu-id="c82e5-115">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c82e5-115">-InstanceId</span></span>
<span data-ttu-id="c82e5-116">Gibt die ID der Aufgabe an, für die dieses Cmdlet den Status nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="c82e5-116">Specifies the ID of the task for which this cmdlet tracks status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TaskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c82e5-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="c82e5-117">-Profile</span></span>
<span data-ttu-id="c82e5-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c82e5-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c82e5-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c82e5-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c82e5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c82e5-120">CommonParameters</span></span>
<span data-ttu-id="c82e5-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c82e5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c82e5-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c82e5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c82e5-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c82e5-123">INPUTS</span></span>

### <span data-ttu-id="c82e5-124">Keine</span><span class="sxs-lookup"><span data-stu-id="c82e5-124">None</span></span>

## <span data-ttu-id="c82e5-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c82e5-125">OUTPUTS</span></span>

### <span data-ttu-id="c82e5-126">JobStatusInfo</span><span class="sxs-lookup"><span data-stu-id="c82e5-126">JobStatusInfo</span></span>
<span data-ttu-id="c82e5-127">Dieses Cmdlet gibt ein **TaskStatusInfo** -Objekt zurück, das die folgenden Felder enthält:</span><span class="sxs-lookup"><span data-stu-id="c82e5-127">This cmdlet returns a **TaskStatusInfo** object which contains the following fields:</span></span> 

- <span data-ttu-id="c82e5-128">**Fehler**.</span><span class="sxs-lookup"><span data-stu-id="c82e5-128">**Error**.</span></span>
<span data-ttu-id="c82e5-129">**ErrorDetails** , die **Code** und **Nachricht** enthält.</span><span class="sxs-lookup"><span data-stu-id="c82e5-129">**ErrorDetails** , which contains **Code** and **Message**.</span></span>
- <span data-ttu-id="c82e5-130">**Task** -Nr.</span><span class="sxs-lookup"><span data-stu-id="c82e5-130">**TaskId**.</span></span>
<span data-ttu-id="c82e5-131">**Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="c82e5-131">**String**.</span></span>
<span data-ttu-id="c82e5-132">Die ID der Aufgabe, für die der Status zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="c82e5-132">The ID of the task for which status is returned.</span></span>
- <span data-ttu-id="c82e5-133">**TaskSteps**.</span><span class="sxs-lookup"><span data-stu-id="c82e5-133">**TaskSteps**.</span></span>
<span data-ttu-id="c82e5-134">**IList \<TaskStep\>**.</span><span class="sxs-lookup"><span data-stu-id="c82e5-134">**IList\<TaskStep\>**.</span></span>
<span data-ttu-id="c82e5-135">Jedes **TaskStep** -Objekt enthält **Details** , **errorCode** , **Nachricht** , **Ergebnis** und **Status**.</span><span class="sxs-lookup"><span data-stu-id="c82e5-135">Each **TaskStep** object contains **Detail** , **ErrorCode** , **Message** , **Result** , and **Status**.</span></span>
- <span data-ttu-id="c82e5-136">**Ergebnis** aus.</span><span class="sxs-lookup"><span data-stu-id="c82e5-136">**Result**.</span></span>
<span data-ttu-id="c82e5-137">**TaskResult** , das das Gesamtergebnis der Aufgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="c82e5-137">**TaskResult** , which contains the overall result of the task.</span></span>
<span data-ttu-id="c82e5-138">Gültige Werte sind: fehlgeschlagen, erfolgreich, PartialSuccess, storniert und ungültig.</span><span class="sxs-lookup"><span data-stu-id="c82e5-138">Valid values are: Failed, Succeeded, PartialSuccess, Cancelled, and Invalid.</span></span>
- <span data-ttu-id="c82e5-139">**Status** aus.</span><span class="sxs-lookup"><span data-stu-id="c82e5-139">**Status**.</span></span>
<span data-ttu-id="c82e5-140">**Taskstatus** , das den allgemeinen Ausführungsstatus der Aufgabe enthält.</span><span class="sxs-lookup"><span data-stu-id="c82e5-140">**TaskStatus** , which contains the overall running status of the task.</span></span>
<span data-ttu-id="c82e5-141">Gültige Werte sind: InProgress, ungültig und abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c82e5-141">Valid values are: Inprogress, Invalid, and Completed.</span></span>
- <span data-ttu-id="c82e5-142">**TaskResult**.</span><span class="sxs-lookup"><span data-stu-id="c82e5-142">**TaskResult**.</span></span>
<span data-ttu-id="c82e5-143">**TaskResult** , ein Wert, der auf Grundlage des **Ergebnisses** und des **Status** berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="c82e5-143">**TaskResult** , a value computed based on **Result** and **Status**.</span></span>
<span data-ttu-id="c82e5-144">Gültige Werte sind: fehlgeschlagen, erfolgreich, InProgress, PartialSuccess, storniert und ungültig.</span><span class="sxs-lookup"><span data-stu-id="c82e5-144">Valid values are: Failed, Succeeded, InProgress, PartialSuccess, Cancelled, and Invalid.</span></span>

## <span data-ttu-id="c82e5-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="c82e5-145">NOTES</span></span>

## <span data-ttu-id="c82e5-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c82e5-146">RELATED LINKS</span></span>

