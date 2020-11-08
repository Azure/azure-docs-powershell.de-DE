---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/remove-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Remove-AzSubscriptionAlias.md
ms.openlocfilehash: 02a32b3e6c39ae66aea8efc37213a6fb3bca0848
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178179"
---
# <span data-ttu-id="63f1d-101">Remove-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="63f1d-101">Remove-AzSubscriptionAlias</span></span>

## <span data-ttu-id="63f1d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="63f1d-102">SYNOPSIS</span></span>
<span data-ttu-id="63f1d-103">Löscht den Abonnement-Alias</span><span class="sxs-lookup"><span data-stu-id="63f1d-103">Deletes the subscription alias</span></span>

## <span data-ttu-id="63f1d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="63f1d-104">SYNTAX</span></span>

```
Remove-AzSubscriptionAlias -AliasName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63f1d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63f1d-105">DESCRIPTION</span></span>
<span data-ttu-id="63f1d-106">Das Cmdlet " **Remove-AzSubscriptionAlias** " entfernt den Abonnement-Alias</span><span class="sxs-lookup"><span data-stu-id="63f1d-106">The **Remove-AzSubscriptionAlias** cmdlet removes the subscription alias</span></span>

## <span data-ttu-id="63f1d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63f1d-107">EXAMPLES</span></span>

### <span data-ttu-id="63f1d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="63f1d-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="63f1d-109">Löscht den Abonnement-Alias</span><span class="sxs-lookup"><span data-stu-id="63f1d-109">Deletes the subscription alias</span></span>

## <span data-ttu-id="63f1d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="63f1d-110">PARAMETERS</span></span>

### <span data-ttu-id="63f1d-111">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="63f1d-111">-AliasName</span></span>
<span data-ttu-id="63f1d-112">Alias für das Abonnement</span><span class="sxs-lookup"><span data-stu-id="63f1d-112">Alias for the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63f1d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63f1d-113">-AsJob</span></span>
<span data-ttu-id="63f1d-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="63f1d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63f1d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63f1d-115">-DefaultProfile</span></span>
<span data-ttu-id="63f1d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="63f1d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63f1d-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="63f1d-117">-Confirm</span></span>
<span data-ttu-id="63f1d-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="63f1d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63f1d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63f1d-119">-WhatIf</span></span>
<span data-ttu-id="63f1d-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="63f1d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63f1d-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63f1d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63f1d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63f1d-122">CommonParameters</span></span>
<span data-ttu-id="63f1d-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63f1d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63f1d-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="63f1d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63f1d-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="63f1d-125">INPUTS</span></span>

### <span data-ttu-id="63f1d-126">Keine</span><span class="sxs-lookup"><span data-stu-id="63f1d-126">None</span></span>

## <span data-ttu-id="63f1d-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="63f1d-127">OUTPUTS</span></span>

### <span data-ttu-id="63f1d-128">Microsoft. Azure. Commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="63f1d-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="63f1d-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="63f1d-129">NOTES</span></span>

## <span data-ttu-id="63f1d-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="63f1d-130">RELATED LINKS</span></span>
