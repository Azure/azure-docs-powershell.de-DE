---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroupsubscription/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroupSubscription.md
ms.openlocfilehash: 39325462d9c2cfb9c06296ff98e5595d2c2c2c06
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007861"
---
# <span data-ttu-id="989d8-101">New-AzManagementGroupSubscription</span><span class="sxs-lookup"><span data-stu-id="989d8-101">New-AzManagementGroupSubscription</span></span>

## <span data-ttu-id="989d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="989d8-102">SYNOPSIS</span></span>
<span data-ttu-id="989d8-103">Fügt ein Abonnement zu einer Verwaltungsgruppe hinzu.</span><span class="sxs-lookup"><span data-stu-id="989d8-103">Adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="989d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="989d8-104">SYNTAX</span></span>

```
New-AzManagementGroupSubscription [-GroupName] <String> [-SubscriptionId] <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="989d8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="989d8-105">DESCRIPTION</span></span>
<span data-ttu-id="989d8-106">Mit dem Cmdlet **New-AzManagementGroupSubscription** wird einer Verwaltungsgruppe ein Abonnement hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="989d8-106">The **New-AzManagementGroupSubscription** cmdlet adds a Subscription to a Management Group.</span></span>

## <span data-ttu-id="989d8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="989d8-107">EXAMPLES</span></span>

### <span data-ttu-id="989d8-108">Beispiel 1: Hinzufügen eines Abonnements zu einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="989d8-108">Example 1: Add Subscription to a Management Group</span></span>
```
PS C:\> New-AzManagementGroupSubscription -GroupName "TestGroup" -SubscriptionId 2120692d-35c3-44c8-81f5-631fa7351726
```

## <span data-ttu-id="989d8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="989d8-109">PARAMETERS</span></span>

### <span data-ttu-id="989d8-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="989d8-110">-DefaultProfile</span></span>
<span data-ttu-id="989d8-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="989d8-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="989d8-112">-GroupName</span><span class="sxs-lookup"><span data-stu-id="989d8-112">-GroupName</span></span>
<span data-ttu-id="989d8-113">Verwaltungsgruppen-ID</span><span class="sxs-lookup"><span data-stu-id="989d8-113">Management Group Id</span></span>

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

### <span data-ttu-id="989d8-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="989d8-114">-PassThru</span></span>
<span data-ttu-id="989d8-115">Zurück `true` zur erfolgreichen Ausführung</span><span class="sxs-lookup"><span data-stu-id="989d8-115">Return `true` on successful execution</span></span>

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

### <span data-ttu-id="989d8-116">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="989d8-116">-SubscriptionId</span></span>
<span data-ttu-id="989d8-117">Abonnement-ID des Abonnements, das der Verwaltung zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="989d8-117">Subscription Id of the subscription associated with the management</span></span>

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

### <span data-ttu-id="989d8-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="989d8-118">-Confirm</span></span>
<span data-ttu-id="989d8-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="989d8-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="989d8-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="989d8-120">-WhatIf</span></span>
<span data-ttu-id="989d8-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="989d8-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="989d8-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="989d8-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="989d8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="989d8-123">CommonParameters</span></span>
<span data-ttu-id="989d8-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="989d8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="989d8-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="989d8-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="989d8-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="989d8-126">INPUTS</span></span>

### <span data-ttu-id="989d8-127">Keine</span><span class="sxs-lookup"><span data-stu-id="989d8-127">None</span></span>

## <span data-ttu-id="989d8-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="989d8-128">OUTPUTS</span></span>

### <span data-ttu-id="989d8-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="989d8-129">System.Boolean</span></span>

## <span data-ttu-id="989d8-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="989d8-130">NOTES</span></span>

## <span data-ttu-id="989d8-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="989d8-131">RELATED LINKS</span></span>
