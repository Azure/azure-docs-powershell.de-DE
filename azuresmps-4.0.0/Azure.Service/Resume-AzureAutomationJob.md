---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 5E5B8102-9E7E-4128-8160-3AA3803B118F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2ff0831e6458a9d587b508acfa2e09948d81d87e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005668"
---
# <span data-ttu-id="05784-101">Resume-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="05784-101">Resume-AzureAutomationJob</span></span>

## <span data-ttu-id="05784-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05784-102">SYNOPSIS</span></span>

<span data-ttu-id="05784-103">Setzt einen angehalten Automatisierungs Auftrag fort.</span><span class="sxs-lookup"><span data-stu-id="05784-103">Resumes a suspended Automation job.</span></span>

## <span data-ttu-id="05784-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="05784-104">SYNTAX</span></span>

```
Resume-AzureAutomationJob -Id <Guid> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="05784-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05784-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="05784-106">Mit dem Cmdlet **Resume-AzureAutomationJob** wird ein angehaltene Microsoft Azure Automation-Auftrag fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="05784-106">The **Resume-AzureAutomationJob** cmdlet resumes a suspended Microsoft Azure Automation job.</span></span>
<span data-ttu-id="05784-107">Verwenden Sie den *ID-* Parameter, um den angehalten-Auftrag anzugeben.</span><span class="sxs-lookup"><span data-stu-id="05784-107">Use the *Id* parameter to specify the suspended job.</span></span>

<span data-ttu-id="05784-108">Verwenden Sie das Suspend-AzureAutomationJob-Cmdlet, um einen Auftrag zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="05784-108">To suspend a job, use the Suspend-AzureAutomationJob cmdlet.</span></span>

## <span data-ttu-id="05784-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05784-109">EXAMPLES</span></span>

### <span data-ttu-id="05784-110">Beispiel 1: Fortsetzen eines angehenden Auftrags</span><span class="sxs-lookup"><span data-stu-id="05784-110">Example 1: Resume a suspended job</span></span>
```
PS C:\> Resume-AzureAutomationJob -AutomationAccountName "Contoso17" -Id 2989b069-24fe-40b9-b3bd-cb7e5eac4b64
```

<span data-ttu-id="05784-111">Mit diesem Befehl wird der Auftrag mit der angegebenen ID fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="05784-111">This command resumes the job that has the specified ID.</span></span>

## <span data-ttu-id="05784-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="05784-112">PARAMETERS</span></span>

### <span data-ttu-id="05784-113">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="05784-113">-AutomationAccountName</span></span>
<span data-ttu-id="05784-114">Gibt den Namen eines Automatisierungs Kontos an.</span><span class="sxs-lookup"><span data-stu-id="05784-114">Specifies the name of an Automation account.</span></span>

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

### <span data-ttu-id="05784-115">-ID</span><span class="sxs-lookup"><span data-stu-id="05784-115">-Id</span></span>
<span data-ttu-id="05784-116">Gibt die ID eines Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="05784-116">Specifies the ID of a job.</span></span>

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

### <span data-ttu-id="05784-117">-Profil</span><span class="sxs-lookup"><span data-stu-id="05784-117">-Profile</span></span>
<span data-ttu-id="05784-118">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="05784-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="05784-119">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="05784-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="05784-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05784-120">CommonParameters</span></span>
<span data-ttu-id="05784-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05784-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05784-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05784-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05784-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05784-123">INPUTS</span></span>

## <span data-ttu-id="05784-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05784-124">OUTPUTS</span></span>

## <span data-ttu-id="05784-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="05784-125">NOTES</span></span>

## <span data-ttu-id="05784-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05784-126">RELATED LINKS</span></span>

[<span data-ttu-id="05784-127">Get-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="05784-127">Get-AzureAutomationJob</span></span>](./Get-AzureAutomationJob.md)

[<span data-ttu-id="05784-128">Stopp-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="05784-128">Stop-AzureAutomationJob</span></span>](./Stop-AzureAutomationJob.md)

[<span data-ttu-id="05784-129">Suspend-AzureAutomationJob</span><span class="sxs-lookup"><span data-stu-id="05784-129">Suspend-AzureAutomationJob</span></span>](./Suspend-AzureAutomationJob.md)


