---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupSubscription.md
ms.openlocfilehash: 843a510376e49a1416129d719c141d72ec80df35
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169097"
---
# <span data-ttu-id="b5751-101">Remove-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="b5751-101">Remove-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="b5751-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5751-102">SYNOPSIS</span></span>
<span data-ttu-id="b5751-103">Entfernt ein Abonnement aus einer Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b5751-103">Removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="b5751-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b5751-104">SYNTAX</span></span>

```
Remove-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5751-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b5751-105">DESCRIPTION</span></span>
<span data-ttu-id="b5751-106">Das **Cmdlet "Remove-AzManagementGroupSubscription"** entfernt ein Abonnement aus einer Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="b5751-106">The **Remove-AzManagementGroupSubscription** cmdlet removes a Subscription from a Management Group.</span></span>

## <span data-ttu-id="b5751-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b5751-107">EXAMPLES</span></span>

### <span data-ttu-id="b5751-108">Beispiel 1: Entfernen eines Abonnements aus einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="b5751-108">Example 1: Remove Subscription from a Management Group</span></span>
```powershell
PS C:\> Remove-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="b5751-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b5751-109">PARAMETERS</span></span>

### <span data-ttu-id="b5751-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5751-110">-DefaultProfile</span></span>
<span data-ttu-id="b5751-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b5751-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5751-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="b5751-112">-GroupName</span></span>
<span data-ttu-id="b5751-113">Management Group Id</span><span class="sxs-lookup"><span data-stu-id="b5751-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5751-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5751-114">-PassThru</span></span>
<span data-ttu-id="b5751-115">Rückgabe `true` bei erfolgreicher Ausführung</span><span class="sxs-lookup"><span data-stu-id="b5751-115">Return `true` on successful execution</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5751-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b5751-116">-SubscriptionId</span></span>
<span data-ttu-id="b5751-117">Abonnement-ID des Abonnements, das der Geschäftsleitung zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="b5751-117">Subscription Id of the subscription associated with the management</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5751-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b5751-118">-Confirm</span></span>
<span data-ttu-id="b5751-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b5751-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5751-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b5751-120">-WhatIf</span></span>
<span data-ttu-id="b5751-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b5751-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5751-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b5751-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5751-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5751-123">CommonParameters</span></span>
<span data-ttu-id="b5751-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5751-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5751-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b5751-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5751-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b5751-126">INPUTS</span></span>

### <span data-ttu-id="b5751-127">Keine</span><span class="sxs-lookup"><span data-stu-id="b5751-127">None</span></span>

## <span data-ttu-id="b5751-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b5751-128">OUTPUTS</span></span>

### <span data-ttu-id="b5751-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b5751-129">System.Boolean</span></span>

## <span data-ttu-id="b5751-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b5751-130">NOTES</span></span>

## <span data-ttu-id="b5751-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b5751-131">RELATED LINKS</span></span>
