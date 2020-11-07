---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
ms.openlocfilehash: a3ef84ef6740eb0d505ff2f9f69670ea83242deb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846648"
---
# <span data-ttu-id="ab1f2-101">New-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="ab1f2-101">New-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="ab1f2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ab1f2-102">SYNOPSIS</span></span>
<span data-ttu-id="ab1f2-103">Fügt ein Abonnement zu einer Verwaltungsgruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="ab1f2-103">Adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="ab1f2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ab1f2-104">SYNTAX</span></span>

```
New-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab1f2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ab1f2-105">DESCRIPTION</span></span>
<span data-ttu-id="ab1f2-106">Mit dem Cmdlet **New-AzManagementGroupSubscription** wird einer Verwaltungsgruppe ein Abonnement hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ab1f2-106">The **New-AzManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="ab1f2-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ab1f2-107">EXAMPLES</span></span>

### <span data-ttu-id="ab1f2-108">Beispiel 1: Hinzufügen eines Abonnements zu einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="ab1f2-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="ab1f2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ab1f2-109">PARAMETERS</span></span>

### <span data-ttu-id="ab1f2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab1f2-110">-DefaultProfile</span></span>
<span data-ttu-id="ab1f2-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ab1f2-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab1f2-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="ab1f2-112">-GroupName</span></span>
<span data-ttu-id="ab1f2-113">Verwaltungsgruppen-ID</span><span class="sxs-lookup"><span data-stu-id="ab1f2-113">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ab1f2-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab1f2-114">-PassThru</span></span>
<span data-ttu-id="ab1f2-115">Zurück `true` zur erfolgreichen Ausführung</span><span class="sxs-lookup"><span data-stu-id="ab1f2-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="ab1f2-116">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="ab1f2-116">-SubscriptionId</span></span>
<span data-ttu-id="ab1f2-117">Abonnement-ID des Abonnements, das der Verwaltung zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="ab1f2-117">Subscription Id of the subscription associated with the management</span></span>

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

### <span data-ttu-id="ab1f2-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ab1f2-118">-Confirm</span></span>
<span data-ttu-id="ab1f2-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ab1f2-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab1f2-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab1f2-120">-WhatIf</span></span>
<span data-ttu-id="ab1f2-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ab1f2-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab1f2-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ab1f2-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab1f2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab1f2-123">CommonParameters</span></span>
<span data-ttu-id="ab1f2-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab1f2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab1f2-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab1f2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab1f2-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ab1f2-126">INPUTS</span></span>

### <span data-ttu-id="ab1f2-127">Keine</span><span class="sxs-lookup"><span data-stu-id="ab1f2-127">None</span></span>

## <span data-ttu-id="ab1f2-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ab1f2-128">OUTPUTS</span></span>

### <span data-ttu-id="ab1f2-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab1f2-129">System.Boolean</span></span>

## <span data-ttu-id="ab1f2-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="ab1f2-130">NOTES</span></span>

## <span data-ttu-id="ab1f2-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ab1f2-131">RELATED LINKS</span></span>
