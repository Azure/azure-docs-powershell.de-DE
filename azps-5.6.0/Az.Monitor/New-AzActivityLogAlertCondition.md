---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 5E854358-CA9D-4336-BA6A-BF7B1FADAB50
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azactivitylogalertcondition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzActivityLogAlertCondition.md
ms.openlocfilehash: f18479f8cf42c68a7c8a8a5d9f45a4542a758212
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932563"
---
# <span data-ttu-id="4cc47-101">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="4cc47-101">New-AzActivityLogAlertCondition</span></span>

## <span data-ttu-id="4cc47-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cc47-102">SYNOPSIS</span></span>
<span data-ttu-id="4cc47-103">Erstellt ein neues Aktivitätsprotokoll-Warnungsbedingungsobjekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="4cc47-103">Creates an new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="4cc47-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4cc47-104">SYNTAX</span></span>

```
New-AzActivityLogAlertCondition -Field <String> -Equal <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4cc47-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4cc47-105">DESCRIPTION</span></span>
<span data-ttu-id="4cc47-106">Das **Cmdlet New-AzActivityLogAlertCondition** erstellt ein neues Aktivitätsprotokollbenachrichtigungsbedingungsobjekt im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="4cc47-106">The **New-AzActivityLogAlertCondition** cmdlet creates new activity log alert condition object in memory.</span></span>

## <span data-ttu-id="4cc47-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4cc47-107">EXAMPLES</span></span>

### <span data-ttu-id="4cc47-108">Beispiel 1: Erstellen eines neuen Aktivitätsprotokoll-Warnungsbedingungsobjekts im Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="4cc47-108">Example 1: Create a new activity log alert condition object in memory.</span></span>
```
PS C:\>$Condition = New-AzActivityLogAlertCondition -Field "Requests" -Equal "OtherField"
PS C:\>Write-Host "Field property value: $($Condition.Field)"
PS C:\>Write-Host "Equals property value: $($Condition.Equals)"

Field property value: Requests
Equals property value: OtherField
```

<span data-ttu-id="4cc47-109">Mit diesem Befehl wird ein neues Aktivitätsprotokollbedingungsobjekt im Arbeitsspeicher erstellt.</span><span class="sxs-lookup"><span data-stu-id="4cc47-109">This command creates a new activity log alert condition object in memory.</span></span>
<span data-ttu-id="4cc47-110">**HINWEIS:** Wenn dieses Cmdlet mit [Set-AzActivityLogAlert](https://docs.microsoft.com/powershell/module/az.monitor/set-azactivitylogalert) verwendet wird, muss mindestens eines dieser Objekte, die als Parameter übergeben werden, sein Feld gleich "Kategorie" haben.</span><span class="sxs-lookup"><span data-stu-id="4cc47-110">**NOTE**: when this cmdlet is used with [Set-AzActivityLogAlert](https://docs.microsoft.com/powershell/module/az.monitor/set-azactivitylogalert) at least one of these objects, passed as parameters, must have its Field equal to "Category".</span></span> <span data-ttu-id="4cc47-111">Andernfalls reagiert das Back-End mit einem 400 (BadRequest.)</span><span class="sxs-lookup"><span data-stu-id="4cc47-111">Otherwise, the backend responds with a 400 (BadRequest.)</span></span>

## <span data-ttu-id="4cc47-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4cc47-112">PARAMETERS</span></span>

### <span data-ttu-id="4cc47-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cc47-113">-DefaultProfile</span></span>
<span data-ttu-id="4cc47-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4cc47-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4cc47-115">-Equal</span><span class="sxs-lookup"><span data-stu-id="4cc47-115">-Equal</span></span>
<span data-ttu-id="4cc47-116">Gibt die Gleichheitseigenschaft für die Blattbedingung an.</span><span class="sxs-lookup"><span data-stu-id="4cc47-116">Specifies the equals property for the leaf condition.</span></span>

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

### <span data-ttu-id="4cc47-117">-Feld</span><span class="sxs-lookup"><span data-stu-id="4cc47-117">-Field</span></span>
<span data-ttu-id="4cc47-118">Gibt das Feld für die Bedingung an.</span><span class="sxs-lookup"><span data-stu-id="4cc47-118">Specifies the field for the condition.</span></span>

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

### <span data-ttu-id="4cc47-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cc47-119">CommonParameters</span></span>
<span data-ttu-id="4cc47-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cc47-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cc47-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4cc47-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cc47-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4cc47-122">INPUTS</span></span>

### <span data-ttu-id="4cc47-123">System.String</span><span class="sxs-lookup"><span data-stu-id="4cc47-123">System.String</span></span>

## <span data-ttu-id="4cc47-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4cc47-124">OUTPUTS</span></span>

### <span data-ttu-id="4cc47-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span><span class="sxs-lookup"><span data-stu-id="4cc47-125">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition</span></span>

## <span data-ttu-id="4cc47-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4cc47-126">NOTES</span></span>

## <span data-ttu-id="4cc47-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4cc47-127">RELATED LINKS</span></span>

[<span data-ttu-id="4cc47-128">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4cc47-128">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="4cc47-129">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4cc47-129">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="4cc47-130">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4cc47-130">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="4cc47-131">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4cc47-131">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="4cc47-132">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="4cc47-132">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="4cc47-133">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="4cc47-133">New-AzActionGroup</span></span>](./Get-AzActionGroup.md)
