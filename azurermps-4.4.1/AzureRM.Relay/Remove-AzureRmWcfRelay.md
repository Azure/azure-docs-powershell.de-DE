---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
ms.openlocfilehash: a774f388690ab2ee0528e94a2a96addecf1687fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504770"
---
# <span data-ttu-id="01f13-101">Remove-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="01f13-101">Remove-AzureRmWcfRelay</span></span>

## <span data-ttu-id="01f13-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="01f13-102">SYNOPSIS</span></span>
<span data-ttu-id="01f13-103">Entfernt die WcfRelay aus dem angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="01f13-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01f13-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="01f13-104">SYNTAX</span></span>

```
Remove-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01f13-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="01f13-105">DESCRIPTION</span></span>
<span data-ttu-id="01f13-106">Das Cmdlet **Remove-AzureRmWcfRelay** entfernt die WcfRelay aus dem angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="01f13-106">The **Remove-AzureRmWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="01f13-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="01f13-107">EXAMPLES</span></span>

### <span data-ttu-id="01f13-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="01f13-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="01f13-109">Entfernt die WcfRelay `TestWCFRelay1` aus dem Namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="01f13-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="01f13-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="01f13-110">PARAMETERS</span></span>

### <span data-ttu-id="01f13-111">-Namespace</span><span class="sxs-lookup"><span data-stu-id="01f13-111">-Namespace</span></span>
<span data-ttu-id="01f13-112">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="01f13-112">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01f13-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01f13-113">-ResourceGroupName</span></span>
<span data-ttu-id="01f13-114">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="01f13-114">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01f13-115">-Name</span><span class="sxs-lookup"><span data-stu-id="01f13-115">-Name</span></span>
<span data-ttu-id="01f13-116">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="01f13-116">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01f13-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="01f13-117">-Confirm</span></span>
<span data-ttu-id="01f13-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01f13-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01f13-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01f13-119">-WhatIf</span></span>
<span data-ttu-id="01f13-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01f13-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01f13-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01f13-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01f13-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01f13-122">-DefaultProfile</span></span>
<span data-ttu-id="01f13-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="01f13-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01f13-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01f13-124">CommonParameters</span></span>
<span data-ttu-id="01f13-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01f13-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01f13-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01f13-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01f13-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="01f13-127">INPUTS</span></span>

### <span data-ttu-id="01f13-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01f13-128">-ResourceGroupName</span></span>
 <span data-ttu-id="01f13-129">System. String</span><span class="sxs-lookup"><span data-stu-id="01f13-129">System.String</span></span>
 

### <span data-ttu-id="01f13-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="01f13-130">-Namespace</span></span>
 <span data-ttu-id="01f13-131">System. String</span><span class="sxs-lookup"><span data-stu-id="01f13-131">System.String</span></span>
 

### <span data-ttu-id="01f13-132">-Name</span><span class="sxs-lookup"><span data-stu-id="01f13-132">-Name</span></span>
 <span data-ttu-id="01f13-133">System. String</span><span class="sxs-lookup"><span data-stu-id="01f13-133">System.String</span></span>

## <span data-ttu-id="01f13-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="01f13-134">OUTPUTS</span></span>

### <span data-ttu-id="01f13-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="01f13-135">System.Object</span></span>

## <span data-ttu-id="01f13-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="01f13-136">NOTES</span></span>

## <span data-ttu-id="01f13-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="01f13-137">RELATED LINKS</span></span>

