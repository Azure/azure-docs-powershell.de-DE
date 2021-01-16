---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
ms.openlocfilehash: 39325462d9c2cfb9c06296ff98e5595d2c2c2c06
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98300504"
---
# <span data-ttu-id="3d60a-101">New-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="3d60a-101">New-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="3d60a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d60a-102">SYNOPSIS</span></span>
<span data-ttu-id="3d60a-103">Fügt einer Verwaltungsgruppe ein Abonnement hinzu.</span><span class="sxs-lookup"><span data-stu-id="3d60a-103">Adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="3d60a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3d60a-104">SYNTAX</span></span>

```
New-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d60a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3d60a-105">DESCRIPTION</span></span>
<span data-ttu-id="3d60a-106">Das **Cmdlet "New-AzManagementGroupSubscription"** fügt einer Verwaltungsgruppe ein Abonnement hinzu.</span><span class="sxs-lookup"><span data-stu-id="3d60a-106">The **New-AzManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="3d60a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3d60a-107">EXAMPLES</span></span>

### <span data-ttu-id="3d60a-108">Beispiel 1: Hinzufügen eines Abonnements zu einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="3d60a-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="3d60a-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d60a-109">PARAMETERS</span></span>

### <span data-ttu-id="3d60a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d60a-110">-DefaultProfile</span></span>
<span data-ttu-id="3d60a-111">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3d60a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d60a-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="3d60a-112">-GroupName</span></span>
<span data-ttu-id="3d60a-113">Management Group Id</span><span class="sxs-lookup"><span data-stu-id="3d60a-113">Management Group Id</span></span>

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

### <span data-ttu-id="3d60a-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d60a-114">-PassThru</span></span>
<span data-ttu-id="3d60a-115">Rückgabe `true` bei erfolgreicher Ausführung</span><span class="sxs-lookup"><span data-stu-id="3d60a-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="3d60a-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3d60a-116">-SubscriptionId</span></span>
<span data-ttu-id="3d60a-117">Abonnement-ID des Abonnements, das der Geschäftsleitung zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="3d60a-117">Subscription Id of the subscription associated with the management</span></span>

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

### <span data-ttu-id="3d60a-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d60a-118">-Confirm</span></span>
<span data-ttu-id="3d60a-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3d60a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d60a-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3d60a-120">-WhatIf</span></span>
<span data-ttu-id="3d60a-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3d60a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d60a-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3d60a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d60a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d60a-123">CommonParameters</span></span>
<span data-ttu-id="3d60a-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d60a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d60a-125">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d60a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d60a-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3d60a-126">INPUTS</span></span>

### <span data-ttu-id="3d60a-127">Keine</span><span class="sxs-lookup"><span data-stu-id="3d60a-127">None</span></span>

## <span data-ttu-id="3d60a-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3d60a-128">OUTPUTS</span></span>

### <span data-ttu-id="3d60a-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3d60a-129">System.Boolean</span></span>

## <span data-ttu-id="3d60a-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3d60a-130">NOTES</span></span>

## <span data-ttu-id="3d60a-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3d60a-131">RELATED LINKS</span></span>
