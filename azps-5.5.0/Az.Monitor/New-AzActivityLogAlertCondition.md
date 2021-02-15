---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: 85cf08b0ade67042c4aa4c4c5ff3253b6af9f2ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159436"
---
# <span data-ttu-id="1757b-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="1757b-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="1757b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1757b-102">SYNOPSIS</span></span>
<span data-ttu-id="1757b-103">Erstellt ein neues Benachrichtigungsobjekt für das Aktivitätsprotokoll im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1757b-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="1757b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1757b-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1757b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1757b-105">DESCRIPTION</span></span>
<span data-ttu-id="1757b-106">Das **Cmdlet "New-AzActivityLogAlertCondition"** erstellt ein neues Warnungsbedingungsobjekt für das Aktivitätsprotokoll im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1757b-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="1757b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1757b-107">EXAMPLES</span></span>

### <span data-ttu-id="1757b-108">Beispiel 1: Erstellen eines neuen Warnungsobjekts für das Aktivitätsprotokoll im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="1757b-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

<span data-ttu-id="1757b-109">Mit diesem Befehl wird ein neues Benachrichtigungsobjekt für das Aktivitätsprotokoll im Arbeitsspeicher erstellt.</span><span class="sxs-lookup"><span data-stu-id="1757b-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="1757b-110">**HINWEIS:** Wenn dieses Cmdlet mit ["Set-AzActivityLogAlert"](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert) verwendet wird, muss mindestens eines dieser Als Parameter übergebenen Objekte das Feld "Kategorie" enthalten.</span><span class="sxs-lookup"><span data-stu-id="1757b-110">**NOTE**: when this cmdlet is used with [Set-AzActivityLogAlert](https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert) at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="1757b-111">Andernfalls reagiert das Back-End mit einem 400-End (BadRequest).)</span><span class="sxs-lookup"><span data-stu-id="1757b-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="1757b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1757b-112">PARAMETERS</span></span>

### <span data-ttu-id="1757b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1757b-113">-DefaultProfile</span></span>
<span data-ttu-id="1757b-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1757b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1757b-115">-Equal</span><span class="sxs-lookup"><span data-stu-id="1757b-115">-Equal</span></span>
<span data-ttu-id="1757b-116">Gibt die Gleichheitseigenschaft für die Blattbedingung an.</span><span class="sxs-lookup"><span data-stu-id="1757b-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="1757b-117">-Field</span><span class="sxs-lookup"><span data-stu-id="1757b-117">-Field</span></span>
<span data-ttu-id="1757b-118">Gibt das Feld für die Bedingung an.</span><span class="sxs-lookup"><span data-stu-id="1757b-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="1757b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1757b-119">CommonParameters</span></span>
<span data-ttu-id="1757b-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1757b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1757b-121">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1757b-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1757b-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1757b-122">INPUTS</span></span>

### <span data-ttu-id="1757b-123">System.String</span><span class="sxs-lookup"><span data-stu-id="1757b-123">System.String</span></span>

## <span data-ttu-id="1757b-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1757b-124">OUTPUTS</span></span>

### <span data-ttu-id="1757b-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="1757b-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="1757b-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1757b-126">NOTES</span></span>

## <span data-ttu-id="1757b-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1757b-127">RELATED LINKS</span></span>

[<span data-ttu-id="1757b-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1757b-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="1757b-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1757b-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="1757b-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1757b-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="1757b-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1757b-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="1757b-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1757b-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="1757b-133">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="1757b-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)
