---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActivityLogAlertCondition.md
ms.openlocfilehash: 058f828037ad546ea5ed66aaadeef579c4908930
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665034"
---
# <span data-ttu-id="e9753-101">New-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="e9753-101">New-AzureRmActivityLogAlertCondition</span></span>

## <span data-ttu-id="e9753-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e9753-102">SYNOPSIS</span></span>
<span data-ttu-id="e9753-103">Erstellt ein neues Aktivitätsprotokoll-Warnungs Konditions Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="e9753-103">Creates an new activity log alert condition object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9753-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9753-104">SYNTAX</span></span>

```
New-AzureRmActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9753-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9753-105">DESCRIPTION</span></span>
<span data-ttu-id="e9753-106">Das Cmdlet **New-AzureRmActivityLogAlertCondition** erstellt ein neues Aktivitätsprotokoll-Warnungs Bedingungsobjekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="e9753-106">The **New-AzureRmActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="e9753-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e9753-107">EXAMPLES</span></span>

### <span data-ttu-id="e9753-108">Beispiel 1: Erstellen eines neuen Aktivitätsprotokoll-Warnungs Bedingungs Objekts im Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="e9753-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$condition = New-AzureRmActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
```

<span data-ttu-id="e9753-109">Dieser Befehl erstellt ein neues Aktivitätsprotokoll-Warnungs Konditions Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="e9753-109">This command creates a new activity log alert condition object in memory.</span></span>

<span data-ttu-id="e9753-110">**Hinweis** : Wenn dieses Cmdlet mit Set-AzureRmActivityLogAlert verwendet wird, muss mindestens eines dieser Objekte, das als Parameter übergeben wird, sein Feld gleich "Category" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e9753-110">**NOTE** : when this cmdlet is used with Set-AzureRmActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="e9753-111">Andernfalls reagiert das Back-End mit einem 400 (BadRequest.)</span><span class="sxs-lookup"><span data-stu-id="e9753-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="e9753-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e9753-112">PARAMETERS</span></span>

### <span data-ttu-id="e9753-113">-Field</span><span class="sxs-lookup"><span data-stu-id="e9753-113">-Field</span></span>
<span data-ttu-id="e9753-114">Gibt das Feld für die Bedingung an.</span><span class="sxs-lookup"><span data-stu-id="e9753-114">Specifies the field for the condition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9753-115">-EQUAL</span><span class="sxs-lookup"><span data-stu-id="e9753-115">-Equal</span></span>
<span data-ttu-id="e9753-116">Gibt die Equals-Eigenschaft für die Blatt Bedingung an.</span><span class="sxs-lookup"><span data-stu-id="e9753-116">Specifies the equals property for the leaf condition.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9753-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9753-117">-DefaultProfile</span></span>
<span data-ttu-id="e9753-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e9753-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9753-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9753-119">CommonParameters</span></span>
<span data-ttu-id="e9753-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9753-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9753-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9753-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9753-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e9753-122">INPUTS</span></span>

## <span data-ttu-id="e9753-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e9753-123">OUTPUTS</span></span>

### <span data-ttu-id="e9753-124">Microsoft. Azure. Management. Monitor. Management. Models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="e9753-124">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="e9753-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="e9753-125">NOTES</span></span>

## <span data-ttu-id="e9753-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e9753-126">RELATED LINKS</span></span>

[<span data-ttu-id="e9753-127">Satz-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e9753-127">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e9753-128">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e9753-128">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e9753-129">Deaktivieren-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e9753-129">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e9753-130">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e9753-130">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e9753-131">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="e9753-131">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="e9753-132">Neu – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="e9753-132">New-AzureRmActionGroup</span></span>](./Get-AzureRmActionGroup.md)
