---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusNamespaceAuthorizationRule.md
ms.openlocfilehash: 08f7f33138ddf9d5226cfc93f263fdec65de3388
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481585"
---
# <span data-ttu-id="12a80-101">Remove-AzureRmServiceBusNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="12a80-101">Remove-AzureRmServiceBusNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="12a80-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="12a80-102">SYNOPSIS</span></span>
<span data-ttu-id="12a80-103">Entfernt die Autorisierungsregel eines ServiceBus-Namespace aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="12a80-103">Removes the authorization rule of a Service Bus namespace from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="12a80-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="12a80-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroupName <String> -Namespace <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12a80-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12a80-105">DESCRIPTION</span></span>
<span data-ttu-id="12a80-106">Das Cmdlet **Remove-AzureRmServiceBusNamespaceAuthorizationRule** entfernt die Autorisierungsregel eines ServiceBus-Namespaces für die angegebene Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="12a80-106">The **Remove-AzureRmServiceBusNamespaceAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace for the specified resource group.</span></span>

## <span data-ttu-id="12a80-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="12a80-107">EXAMPLES</span></span>

### <span data-ttu-id="12a80-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="12a80-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusNamespaceAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -AuthorizationRuleName AuthoRule1
```

<span data-ttu-id="12a80-109">Entfernt die Autorisierungsregel `SBAuthoRule1` für Namespace `SB-Example1` aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="12a80-109">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

## <span data-ttu-id="12a80-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="12a80-110">PARAMETERS</span></span>

### <span data-ttu-id="12a80-111">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="12a80-111">-Confirm</span></span>
<span data-ttu-id="12a80-112">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12a80-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a80-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12a80-113">-WhatIf</span></span>
<span data-ttu-id="12a80-114">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12a80-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12a80-115">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12a80-115">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a80-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12a80-116">-DefaultProfile</span></span>
<span data-ttu-id="12a80-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="12a80-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="12a80-118">-Name</span><span class="sxs-lookup"><span data-stu-id="12a80-118">-Name</span></span>
<span data-ttu-id="12a80-119">Name des Namespace-AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="12a80-119">Namespace AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a80-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="12a80-120">-Namespace</span></span>
<span data-ttu-id="12a80-121">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="12a80-121">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a80-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12a80-122">-ResourceGroupName</span></span>
<span data-ttu-id="12a80-123">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="12a80-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12a80-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12a80-124">CommonParameters</span></span>
<span data-ttu-id="12a80-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12a80-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12a80-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12a80-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12a80-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="12a80-127">INPUTS</span></span>

### <span data-ttu-id="12a80-128">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="12a80-128">-ResourceGroup</span></span>
 <span data-ttu-id="12a80-129">System. String</span><span class="sxs-lookup"><span data-stu-id="12a80-129">System.String</span></span>

### <span data-ttu-id="12a80-130">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="12a80-130">-NamespaceName</span></span>
 <span data-ttu-id="12a80-131">System. String</span><span class="sxs-lookup"><span data-stu-id="12a80-131">System.String</span></span>

### <span data-ttu-id="12a80-132">-Authorizationrulename</span><span class="sxs-lookup"><span data-stu-id="12a80-132">-AuthorizationRuleName</span></span>
 <span data-ttu-id="12a80-133">System. String</span><span class="sxs-lookup"><span data-stu-id="12a80-133">System.String</span></span>

## <span data-ttu-id="12a80-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="12a80-134">OUTPUTS</span></span>

### <span data-ttu-id="12a80-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="12a80-135">System.Boolean</span></span>

## <span data-ttu-id="12a80-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="12a80-136">NOTES</span></span>

## <span data-ttu-id="12a80-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="12a80-137">RELATED LINKS</span></span>

