---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: e141e2af2dea2a07a9a64ab25c2417ffb6842837
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475206"
---
# <span data-ttu-id="86414-101">Set-AzureRmContext</span><span class="sxs-lookup"><span data-stu-id="86414-101">Set-AzureRmContext</span></span>

## <span data-ttu-id="86414-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="86414-102">SYNOPSIS</span></span>
<span data-ttu-id="86414-103">Legt den Mandanten, das Abonnement und die Umgebung für Cmdlets fest, die in der aktuellen Sitzung verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="86414-103">Sets the tenant, subscription, and environment for cmdlets to use in the current session.</span></span>

## <span data-ttu-id="86414-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="86414-104">SYNTAX</span></span>

### <span data-ttu-id="86414-105">Abonnementname (Standard)</span><span class="sxs-lookup"><span data-stu-id="86414-105">SubscriptionName (Default)</span></span>
```
Set-AzureRmContext [-SubscriptionName <String>] [-TenantId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86414-106">Kontext</span><span class="sxs-lookup"><span data-stu-id="86414-106">Context</span></span>
```
Set-AzureRmContext -Context <PSAzureContext> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86414-107">SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="86414-107">SubscriptionId</span></span>
```
Set-AzureRmContext [-TenantId <String>] [-SubscriptionId <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86414-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="86414-108">DESCRIPTION</span></span>
<span data-ttu-id="86414-109">Das Set-AzureRmContext-Cmdlet legt Authentifizierungsinformationen für Cmdlets fest, die Sie in der aktuellen Sitzung ausführen.</span><span class="sxs-lookup"><span data-stu-id="86414-109">The Set-AzureRmContext cmdlet sets authentication information for cmdlets that you run in the current session.</span></span>
<span data-ttu-id="86414-110">Der Kontext umfasst Mandanten-, Abonnement-und Umgebungsinformationen.</span><span class="sxs-lookup"><span data-stu-id="86414-110">The context includes tenant, subscription, and environment information.</span></span>

## <span data-ttu-id="86414-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="86414-111">EXAMPLES</span></span>

### <span data-ttu-id="86414-112">Beispiel 1: Einrichten des Abonnement Kontexts</span><span class="sxs-lookup"><span data-stu-id="86414-112">Example 1: Set the subscription context</span></span>
```
PS C:\>Set-AzureRmContext -SubscriptionId "xxxx-xxxx-xxxx-xxxx"

Account      : PFuller@contoso.com
Environment  : AzureCloud
Subscription : xxxx-xxxx-xxxx-xxxx
Tenant       : yyyy-yyyy-yyyy-yyyy
```

<span data-ttu-id="86414-113">Mit diesem Befehl wird der Kontext für die Verwendung des angegebenen Abonnements festgelegt.</span><span class="sxs-lookup"><span data-stu-id="86414-113">This command sets the context to use the specified subscription.</span></span>

## <span data-ttu-id="86414-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="86414-114">PARAMETERS</span></span>

### <span data-ttu-id="86414-115">-Context</span><span class="sxs-lookup"><span data-stu-id="86414-115">-Context</span></span>
<span data-ttu-id="86414-116">Gibt den Kontext für die aktuelle Sitzung an.</span><span class="sxs-lookup"><span data-stu-id="86414-116">Specifies the context for the current session.</span></span>

```yaml
Type: PSAzureContext
Parameter Sets: Context
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86414-117">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="86414-117">-SubscriptionId</span></span>
<span data-ttu-id="86414-118">Gibt die Abonnement-ID für den Kontext an, den dieses Cmdlet für die aktuelle Sitzung festlegt.</span><span class="sxs-lookup"><span data-stu-id="86414-118">Specifies the subscription ID for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86414-119">-Abonnementname</span><span class="sxs-lookup"><span data-stu-id="86414-119">-SubscriptionName</span></span>
<span data-ttu-id="86414-120">Gibt den Abonnement Namen für den Kontext an, den dieses Cmdlet für die aktuelle Sitzung festlegt.</span><span class="sxs-lookup"><span data-stu-id="86414-120">Specifies the subscription name for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86414-121">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="86414-121">-TenantId</span></span>
<span data-ttu-id="86414-122">Gibt die ID des Mandanten für den Kontext an, den dieses Cmdlet für die aktuelle Sitzung festlegt.</span><span class="sxs-lookup"><span data-stu-id="86414-122">Specifies the ID of the tenant for the context that this cmdlet sets for the current session.</span></span>

```yaml
Type: String
Parameter Sets: SubscriptionName, SubscriptionId
Aliases: Domain

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86414-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="86414-123">-Confirm</span></span>
<span data-ttu-id="86414-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="86414-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86414-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86414-125">-WhatIf</span></span>
<span data-ttu-id="86414-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="86414-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="86414-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="86414-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86414-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86414-128">CommonParameters</span></span>
<span data-ttu-id="86414-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86414-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86414-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86414-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86414-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="86414-131">INPUTS</span></span>

## <span data-ttu-id="86414-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="86414-132">OUTPUTS</span></span>

### <span data-ttu-id="86414-133">PSAzureContext</span><span class="sxs-lookup"><span data-stu-id="86414-133">PSAzureContext</span></span>

## <span data-ttu-id="86414-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="86414-134">NOTES</span></span>

## <span data-ttu-id="86414-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="86414-135">RELATED LINKS</span></span>

[<span data-ttu-id="86414-136">Get-AzureRMContext</span><span class="sxs-lookup"><span data-stu-id="86414-136">Get-AzureRMContext</span></span>]()

