---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubKey.md
ms.openlocfilehash: 8be39cb4b4b173d3b87efbf0b7ecea72ae233061
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663262"
---
# <span data-ttu-id="26caa-101">New-AzureRmEventHubKey</span><span class="sxs-lookup"><span data-stu-id="26caa-101">New-AzureRmEventHubKey</span></span>

## <span data-ttu-id="26caa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="26caa-102">SYNOPSIS</span></span>
<span data-ttu-id="26caa-103">Erstellt einen neuen primären oder sekundären Schlüssel für die angegebene Autorisierungsregel für Ereignis Hubs.</span><span class="sxs-lookup"><span data-stu-id="26caa-103">Creates a new primary or secondary key for the specified Event Hubs authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26caa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="26caa-104">SYNTAX</span></span>

### <span data-ttu-id="26caa-105">NamespaceAuthorizationRuleSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="26caa-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-RegenerateKey] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26caa-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="26caa-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubKey [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-RegenerateKey] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="26caa-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26caa-107">DESCRIPTION</span></span>
<span data-ttu-id="26caa-108">Das New-AzureRmEventHubKey-Cmdlet generiert den primären oder sekundären SAS-Schlüssel für die angegebene Autorisierungsregel für Ereignis Hubs erneut.</span><span class="sxs-lookup"><span data-stu-id="26caa-108">The New-AzureRmEventHubKey cmdlet regenerates the primary or secondary SAS key for the specified Event Hubs authorization rule.</span></span>

## <span data-ttu-id="26caa-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26caa-109">EXAMPLES</span></span>

### <span data-ttu-id="26caa-110">Beispiel 1,1</span><span class="sxs-lookup"><span data-stu-id="26caa-110">Example 1.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="26caa-111">Generiert den Primärschlüssel für die Autorisierungsregel \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="26caa-111">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="26caa-112">Beispiel 1,2</span><span class="sxs-lookup"><span data-stu-id="26caa-112">Example 1.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey PrimaryKey
```

<span data-ttu-id="26caa-113">Generiert den Primärschlüssel für die Autorisierungsregel \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="26caa-113">Regenerates the primary key for the authorization rule \`MyAuthRuleName\`.</span></span>

### <span data-ttu-id="26caa-114">Beispiel 2,1</span><span class="sxs-lookup"><span data-stu-id="26caa-114">Example 2.1</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

### <span data-ttu-id="26caa-115">Beispiel 2,2</span><span class="sxs-lookup"><span data-stu-id="26caa-115">Example 2.2</span></span>
```
PS C:\> New-AzureRmEventHubKey -ResourceGroup MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName -RegenerateKey SecondaryKey
```

<span data-ttu-id="26caa-116">Generiert den Sekundärschlüssel für die Autorisierungsregel \` MyAuthRuleName \` .</span><span class="sxs-lookup"><span data-stu-id="26caa-116">Regenerates the secondary key for the authorization rule \`MyAuthRuleName\`.</span></span>

## <span data-ttu-id="26caa-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="26caa-117">PARAMETERS</span></span>

### <span data-ttu-id="26caa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26caa-118">-DefaultProfile</span></span>
<span data-ttu-id="26caa-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="26caa-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26caa-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="26caa-120">-EventHub</span></span>
<span data-ttu-id="26caa-121">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="26caa-121">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26caa-122">-Name</span><span class="sxs-lookup"><span data-stu-id="26caa-122">-Name</span></span>
<span data-ttu-id="26caa-123">AuthorizationRule-Name</span><span class="sxs-lookup"><span data-stu-id="26caa-123">AuthorizationRule Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26caa-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="26caa-124">-Namespace</span></span>
<span data-ttu-id="26caa-125">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="26caa-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26caa-126">-RegenerateKey</span><span class="sxs-lookup"><span data-stu-id="26caa-126">-RegenerateKey</span></span>
<span data-ttu-id="26caa-127">Schlüssel neu generieren-"Primärschlüssel"/"SecondaryKey"</span><span class="sxs-lookup"><span data-stu-id="26caa-127">Regenerate Keys - 'PrimaryKey'/'SecondaryKey'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: PrimaryKey, SecondaryKey

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26caa-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26caa-128">-ResourceGroupName</span></span>
<span data-ttu-id="26caa-129">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="26caa-129">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="26caa-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="26caa-130">-Confirm</span></span>
<span data-ttu-id="26caa-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="26caa-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26caa-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26caa-132">-WhatIf</span></span>
<span data-ttu-id="26caa-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26caa-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26caa-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26caa-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26caa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26caa-135">CommonParameters</span></span>
<span data-ttu-id="26caa-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26caa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="26caa-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26caa-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26caa-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="26caa-138">INPUTS</span></span>

### <span data-ttu-id="26caa-139">System. String</span><span class="sxs-lookup"><span data-stu-id="26caa-139">System.String</span></span>


## <span data-ttu-id="26caa-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="26caa-140">OUTPUTS</span></span>

### <span data-ttu-id="26caa-141">Microsoft. Azure. Commands. EventHub. Models. PSListKeysAttributes</span><span class="sxs-lookup"><span data-stu-id="26caa-141">Microsoft.Azure.Commands.EventHub.Models.PSListKeysAttributes</span></span>


## <span data-ttu-id="26caa-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="26caa-142">NOTES</span></span>

## <span data-ttu-id="26caa-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="26caa-143">RELATED LINKS</span></span>
