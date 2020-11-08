---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Subscription.dll-Help.xml
Module Name: Az.Subscription
online version: https://docs.microsoft.com/en-us/powershell/module/az.subscription/get-azsubscriptionalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Subscription/Subscription/help/Get-AzSubscriptionAlias.md
ms.openlocfilehash: a76c993abb254b1e24200267bf0195cb613d8207
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178184"
---
# <span data-ttu-id="62855-101">Get-AzSubscriptionAlias</span><span class="sxs-lookup"><span data-stu-id="62855-101">Get-AzSubscriptionAlias</span></span>

## <span data-ttu-id="62855-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="62855-102">SYNOPSIS</span></span>
<span data-ttu-id="62855-103">Ruft Alias Details für Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="62855-103">Gets subscription alias details</span></span>

## <span data-ttu-id="62855-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="62855-104">SYNTAX</span></span>

```
Get-AzSubscriptionAlias [-AliasName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62855-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="62855-105">DESCRIPTION</span></span>
<span data-ttu-id="62855-106">Das Cmdlet " **Get-AzSubscriptionAlias** " ruft Details zum Abonnement-Alias ab.</span><span class="sxs-lookup"><span data-stu-id="62855-106">The **Get-AzSubscriptionAlias** cmdlet gets subscription alias details.</span></span>

## <span data-ttu-id="62855-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="62855-107">EXAMPLES</span></span>

### <span data-ttu-id="62855-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="62855-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSubscriptionAlias -AliasName "ExistingAliasName"
```

<span data-ttu-id="62855-109">Ruft Alias Details für Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="62855-109">Gets subscription alias details</span></span>

## <span data-ttu-id="62855-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="62855-110">PARAMETERS</span></span>

### <span data-ttu-id="62855-111">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="62855-111">-AliasName</span></span>
<span data-ttu-id="62855-112">Alias für das Abonnement</span><span class="sxs-lookup"><span data-stu-id="62855-112">Alias for the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62855-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62855-113">-AsJob</span></span>
<span data-ttu-id="62855-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="62855-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62855-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62855-115">-DefaultProfile</span></span>
<span data-ttu-id="62855-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="62855-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62855-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="62855-117">-Confirm</span></span>
<span data-ttu-id="62855-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="62855-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62855-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62855-119">-WhatIf</span></span>
<span data-ttu-id="62855-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="62855-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62855-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="62855-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62855-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62855-122">CommonParameters</span></span>
<span data-ttu-id="62855-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62855-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62855-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62855-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62855-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="62855-125">INPUTS</span></span>

### <span data-ttu-id="62855-126">Keine</span><span class="sxs-lookup"><span data-stu-id="62855-126">None</span></span>

## <span data-ttu-id="62855-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="62855-127">OUTPUTS</span></span>

### <span data-ttu-id="62855-128">Microsoft. Azure. Commands. Subscription. Models. PSAzureSubscription</span><span class="sxs-lookup"><span data-stu-id="62855-128">Microsoft.Azure.Commands.Subscription.Models.PSAzureSubscription</span></span>

## <span data-ttu-id="62855-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="62855-129">NOTES</span></span>

## <span data-ttu-id="62855-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="62855-130">RELATED LINKS</span></span>
