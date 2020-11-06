---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmRelayNamespace.md
ms.openlocfilehash: d0ac732a0feaffa187ec33d60f9587a7a6a1cff1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503218"
---
# <span data-ttu-id="bcbcf-101">Remove-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="bcbcf-101">Remove-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="bcbcf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bcbcf-102">SYNOPSIS</span></span>
<span data-ttu-id="bcbcf-103">Entfernt den Namespace aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-103">Removes the namespace from the specified resource group.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcbcf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bcbcf-104">SYNTAX</span></span>

```
Remove-AzureRmRelayNamespace [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcbcf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bcbcf-105">DESCRIPTION</span></span>
<span data-ttu-id="bcbcf-106">Das Cmdlet **Remove-AzureRmRelayNamespace** entfernt den Namespace aus der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-106">The **Remove-AzureRmRelayNamespace** cmdlet removes the namespace from the specified resource group.</span></span>

## <span data-ttu-id="bcbcf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bcbcf-107">EXAMPLES</span></span>

### <span data-ttu-id="bcbcf-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bcbcf-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="bcbcf-109">Entfernt den Relay `TestNameSpace-Relay1` -Namespace aus der angegebenen Ressourcengruppe `Default-ServiceBus-WestUS` .</span><span class="sxs-lookup"><span data-stu-id="bcbcf-109">Removes the Relay namespace `TestNameSpace-Relay1` from the specified resource group `Default-ServiceBus-WestUS`.</span></span>

## <span data-ttu-id="bcbcf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bcbcf-110">PARAMETERS</span></span>

### <span data-ttu-id="bcbcf-111">-Name</span><span class="sxs-lookup"><span data-stu-id="bcbcf-111">-Name</span></span>
<span data-ttu-id="bcbcf-112">Name des Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-112">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="bcbcf-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcbcf-113">-ResourceGroupName</span></span>
<span data-ttu-id="bcbcf-114">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-114">Resource Group Name.</span></span>

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

### <span data-ttu-id="bcbcf-115">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bcbcf-115">-Confirm</span></span>
<span data-ttu-id="bcbcf-116">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcbcf-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcbcf-117">-WhatIf</span></span>
<span data-ttu-id="bcbcf-118">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcbcf-119">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcbcf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcbcf-120">-DefaultProfile</span></span>
<span data-ttu-id="bcbcf-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bcbcf-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcbcf-122">CommonParameters</span></span>
<span data-ttu-id="bcbcf-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcbcf-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcbcf-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcbcf-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcbcf-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bcbcf-125">INPUTS</span></span>

### <span data-ttu-id="bcbcf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcbcf-126">-ResourceGroupName</span></span>
 <span data-ttu-id="bcbcf-127">System. String</span><span class="sxs-lookup"><span data-stu-id="bcbcf-127">System.String</span></span>

### <span data-ttu-id="bcbcf-128">-Name</span><span class="sxs-lookup"><span data-stu-id="bcbcf-128">-Name</span></span>
 <span data-ttu-id="bcbcf-129">System. String</span><span class="sxs-lookup"><span data-stu-id="bcbcf-129">System.String</span></span>

## <span data-ttu-id="bcbcf-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bcbcf-130">OUTPUTS</span></span>

### <span data-ttu-id="bcbcf-131">System. Object</span><span class="sxs-lookup"><span data-stu-id="bcbcf-131">System.Object</span></span>

## <span data-ttu-id="bcbcf-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="bcbcf-132">NOTES</span></span>

## <span data-ttu-id="bcbcf-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bcbcf-133">RELATED LINKS</span></span>

