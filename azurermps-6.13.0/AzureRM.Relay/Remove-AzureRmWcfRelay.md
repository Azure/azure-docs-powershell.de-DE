---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/remove-azurermwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Remove-AzureRmWcfRelay.md
ms.openlocfilehash: 5e49497f8784e9686c84cb75dde4b8fd4297578d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482142"
---
# <span data-ttu-id="a0293-101">Remove-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="a0293-101">Remove-AzureRmWcfRelay</span></span>

## <span data-ttu-id="a0293-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0293-102">SYNOPSIS</span></span>
<span data-ttu-id="a0293-103">Entfernt die WcfRelay aus dem angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="a0293-103">Removes the WcfRelay from the specified Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0293-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0293-104">SYNTAX</span></span>

```
Remove-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0293-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0293-105">DESCRIPTION</span></span>
<span data-ttu-id="a0293-106">Das Cmdlet **Remove-AzureRmWcfRelay** entfernt die WcfRelay aus dem angegebenen Relay-Namespace.</span><span class="sxs-lookup"><span data-stu-id="a0293-106">The **Remove-AzureRmWcfRelay** cmdlet removes the WcfRelay from the specified Relay namespace.</span></span>

## <span data-ttu-id="a0293-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0293-107">EXAMPLES</span></span>

### <span data-ttu-id="a0293-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a0293-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="a0293-109">Entfernt die WcfRelay `TestWCFRelay1` aus dem Namespace `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="a0293-109">Removes the WcfRelay `TestWCFRelay1` from the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="a0293-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0293-110">PARAMETERS</span></span>

### <span data-ttu-id="a0293-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0293-111">-DefaultProfile</span></span>
<span data-ttu-id="a0293-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a0293-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0293-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a0293-113">-Name</span></span>
<span data-ttu-id="a0293-114">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="a0293-114">WcfRelay Name.</span></span>

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

### <span data-ttu-id="a0293-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a0293-115">-Namespace</span></span>
<span data-ttu-id="a0293-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="a0293-116">Namespace Name.</span></span>

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

### <span data-ttu-id="a0293-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0293-117">-ResourceGroupName</span></span>
<span data-ttu-id="a0293-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a0293-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="a0293-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a0293-119">-Confirm</span></span>
<span data-ttu-id="a0293-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0293-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0293-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0293-121">-WhatIf</span></span>
<span data-ttu-id="a0293-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0293-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0293-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0293-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0293-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0293-124">CommonParameters</span></span>
<span data-ttu-id="a0293-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0293-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a0293-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0293-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0293-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0293-127">INPUTS</span></span>

### <span data-ttu-id="a0293-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a0293-128">System.String</span></span>


## <span data-ttu-id="a0293-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0293-129">OUTPUTS</span></span>

### <span data-ttu-id="a0293-130">System. void</span><span class="sxs-lookup"><span data-stu-id="a0293-130">System.Void</span></span>


## <span data-ttu-id="a0293-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0293-131">NOTES</span></span>

## <span data-ttu-id="a0293-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0293-132">RELATED LINKS</span></span>
