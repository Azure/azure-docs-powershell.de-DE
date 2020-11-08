---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: 4932445406e19cbc05f5e2680871a03ae6f40f60
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008392"
---
# <span data-ttu-id="8dd06-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="8dd06-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="8dd06-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8dd06-102">SYNOPSIS</span></span>
<span data-ttu-id="8dd06-103">Erstellt ein neues Aktivitätsprotokoll-Warnungs Konditions Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="8dd06-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="8dd06-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8dd06-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8dd06-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8dd06-105">DESCRIPTION</span></span>
<span data-ttu-id="8dd06-106">Das Cmdlet **New-AzActivityLogAlertCondition** erstellt ein neues Aktivitätsprotokoll-Warnungs Bedingungsobjekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="8dd06-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="8dd06-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8dd06-107">EXAMPLES</span></span>

### <span data-ttu-id="8dd06-108">Beispiel 1: Erstellen eines neuen Aktivitätsprotokoll-Warnungs Bedingungs Objekts im Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="8dd06-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

<span data-ttu-id="8dd06-109">Dieser Befehl erstellt ein neues Aktivitätsprotokoll-Warnungs Konditions Objekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="8dd06-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="8dd06-110">**Hinweis** : Wenn dieses Cmdlet mit Set-AzActivityLogAlert verwendet wird, muss mindestens eines dieser Objekte, das als Parameter übergeben wird, sein Feld gleich "Category" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8dd06-110">**NOTE** : when this cmdlet is used with Set-AzActivityLogAlert at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="8dd06-111">Andernfalls reagiert das Back-End mit einem 400 (BadRequest.)</span><span class="sxs-lookup"><span data-stu-id="8dd06-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="8dd06-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="8dd06-112">PARAMETERS</span></span>

### <span data-ttu-id="8dd06-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dd06-113">-DefaultProfile</span></span>
<span data-ttu-id="8dd06-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8dd06-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8dd06-115">-EQUAL</span><span class="sxs-lookup"><span data-stu-id="8dd06-115">-Equal</span></span>
<span data-ttu-id="8dd06-116">Gibt die Equals-Eigenschaft für die Blatt Bedingung an.</span><span class="sxs-lookup"><span data-stu-id="8dd06-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="8dd06-117">-Field</span><span class="sxs-lookup"><span data-stu-id="8dd06-117">-Field</span></span>
<span data-ttu-id="8dd06-118">Gibt das Feld für die Bedingung an.</span><span class="sxs-lookup"><span data-stu-id="8dd06-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="8dd06-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dd06-119">CommonParameters</span></span>
<span data-ttu-id="8dd06-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8dd06-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dd06-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8dd06-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dd06-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8dd06-122">INPUTS</span></span>

### <span data-ttu-id="8dd06-123">System. String</span><span class="sxs-lookup"><span data-stu-id="8dd06-123">System.String</span></span>

## <span data-ttu-id="8dd06-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8dd06-124">OUTPUTS</span></span>

### <span data-ttu-id="8dd06-125">Microsoft. Azure. Management. Monitor. Management. Models. ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="8dd06-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="8dd06-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="8dd06-126">NOTES</span></span>

## <span data-ttu-id="8dd06-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8dd06-127">RELATED LINKS</span></span>

[<span data-ttu-id="8dd06-128">Satz-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8dd06-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="8dd06-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8dd06-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="8dd06-130">Deaktivieren-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8dd06-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="8dd06-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8dd06-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="8dd06-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="8dd06-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="8dd06-133">Neu – AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="8dd06-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)
