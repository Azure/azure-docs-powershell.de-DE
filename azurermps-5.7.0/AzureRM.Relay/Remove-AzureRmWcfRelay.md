---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
ms.openlocfilehash: 02949f3a16c9a259e645a035ce3e762db9582024
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480994"
---
# <span data-ttu-id="35af8-101">Remove-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="35af8-101">Remove-AzureRmWcfRelay</span></span>

## <span data-ttu-id="35af8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35af8-102">SYNOPSIS</span></span>
<span data-ttu-id="35af8-103">Entfernt die WcfRelay aus dem angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="35af8-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35af8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35af8-104">SYNTAX</span></span>

```
Remove-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35af8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35af8-105">DESCRIPTION</span></span>
<span data-ttu-id="35af8-106">Das Cmdlet **Remove-AzureRmWcfRelay** entfernt die WcfRelay aus dem angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="35af8-106">The **Remove-AzureRmWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="35af8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35af8-107">EXAMPLES</span></span>

### <span data-ttu-id="35af8-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="35af8-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="35af8-109">Entfernt die WcfRelay `TestWCFRelay1` aus dem Namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="35af8-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="35af8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="35af8-110">PARAMETERS</span></span>

### <span data-ttu-id="35af8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35af8-111">-DefaultProfile</span></span>
<span data-ttu-id="35af8-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="35af8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35af8-113">-Name</span><span class="sxs-lookup"><span data-stu-id="35af8-113">-Name</span></span>
<span data-ttu-id="35af8-114">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="35af8-114">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35af8-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="35af8-115">-Namespace</span></span>
<span data-ttu-id="35af8-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="35af8-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35af8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35af8-117">-ResourceGroupName</span></span>
<span data-ttu-id="35af8-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="35af8-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35af8-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="35af8-119">-Confirm</span></span>
<span data-ttu-id="35af8-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="35af8-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35af8-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35af8-121">-WhatIf</span></span>
<span data-ttu-id="35af8-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="35af8-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35af8-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="35af8-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35af8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35af8-124">CommonParameters</span></span>
<span data-ttu-id="35af8-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35af8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35af8-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35af8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35af8-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35af8-127">INPUTS</span></span>

### <span data-ttu-id="35af8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35af8-128">-ResourceGroupName</span></span>
 <span data-ttu-id="35af8-129">System. String</span><span class="sxs-lookup"><span data-stu-id="35af8-129">System.String</span></span>
 

### <span data-ttu-id="35af8-130">-Namespace</span><span class="sxs-lookup"><span data-stu-id="35af8-130">-Namespace</span></span>
 <span data-ttu-id="35af8-131">System. String</span><span class="sxs-lookup"><span data-stu-id="35af8-131">System.String</span></span>
 

### <span data-ttu-id="35af8-132">-Name</span><span class="sxs-lookup"><span data-stu-id="35af8-132">-Name</span></span>
 <span data-ttu-id="35af8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="35af8-133">System.String</span></span>

## <span data-ttu-id="35af8-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35af8-134">OUTPUTS</span></span>

### <span data-ttu-id="35af8-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="35af8-135">System.Object</span></span>

## <span data-ttu-id="35af8-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="35af8-136">NOTES</span></span>

## <span data-ttu-id="35af8-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35af8-137">RELATED LINKS</span></span>

