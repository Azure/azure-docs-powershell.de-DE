---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 196d0eba5119ab984f9ffc632a301d3e65157f63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663162"
---
# <span data-ttu-id="a16db-101">Remove-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a16db-101">Remove-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="a16db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a16db-102">SYNOPSIS</span></span>
<span data-ttu-id="a16db-103">Entfernt die angegebene virtuelle Netzwerkregel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a16db-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a16db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a16db-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a16db-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a16db-105">DESCRIPTION</span></span>
<span data-ttu-id="a16db-106">Das Cmdlet **Remove-AzureRmDataLakeStoreVirtualNetworkRule** entfernt die angegebene virtuelle Netzwerkregel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a16db-106">The **Remove-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="a16db-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a16db-107">EXAMPLES</span></span>

### <span data-ttu-id="a16db-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a16db-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="a16db-109">Entfernt die virtuelle Netzwerkregel "myVNET" aus dem Konto "DLS"</span><span class="sxs-lookup"><span data-stu-id="a16db-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="a16db-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a16db-110">PARAMETERS</span></span>

### <span data-ttu-id="a16db-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="a16db-111">-Account</span></span>
<span data-ttu-id="a16db-112">Das Data Lake Store-Konto zum Aktualisieren der virtuellen Netzwerkregel in</span><span class="sxs-lookup"><span data-stu-id="a16db-112">The Data Lake Store account to update the virtual network rule in</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a16db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a16db-113">-DefaultProfile</span></span>
<span data-ttu-id="a16db-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a16db-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a16db-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a16db-115">-Name</span></span>
<span data-ttu-id="a16db-116">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a16db-116">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a16db-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a16db-117">-PassThru</span></span>
<span data-ttu-id="a16db-118">Gibt an, dass eine boolesche Antwort zurückgegeben werden soll, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="a16db-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="a16db-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a16db-119">-Confirm</span></span>
<span data-ttu-id="a16db-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a16db-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a16db-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a16db-121">-WhatIf</span></span>
<span data-ttu-id="a16db-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a16db-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a16db-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a16db-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a16db-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a16db-124">CommonParameters</span></span>
<span data-ttu-id="a16db-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a16db-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a16db-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a16db-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a16db-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a16db-127">INPUTS</span></span>

### <span data-ttu-id="a16db-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a16db-128">System.String</span></span>

### <span data-ttu-id="a16db-129">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="a16db-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a16db-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a16db-130">OUTPUTS</span></span>

### <span data-ttu-id="a16db-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a16db-131">System.Boolean</span></span>

## <span data-ttu-id="a16db-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="a16db-132">NOTES</span></span>

## <span data-ttu-id="a16db-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a16db-133">RELATED LINKS</span></span>
