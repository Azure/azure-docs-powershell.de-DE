---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 7faa09d45082e6443ab389ebe3a355c9656bb8e2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651516"
---
# <span data-ttu-id="385aa-101">Remove-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="385aa-101">Remove-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="385aa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="385aa-102">SYNOPSIS</span></span>
<span data-ttu-id="385aa-103">Entfernt die angegebene virtuelle Netzwerkregel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="385aa-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="385aa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="385aa-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="385aa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="385aa-105">DESCRIPTION</span></span>
<span data-ttu-id="385aa-106">Das Cmdlet **Remove-AzDataLakeStoreVirtualNetworkRule** entfernt die angegebene virtuelle Netzwerkregel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="385aa-106">The **Remove-AzDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="385aa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="385aa-107">EXAMPLES</span></span>

### <span data-ttu-id="385aa-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="385aa-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="385aa-109">Entfernt die virtuelle Netzwerkregel "myVNET" aus dem Konto "DLS"</span><span class="sxs-lookup"><span data-stu-id="385aa-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="385aa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="385aa-110">PARAMETERS</span></span>

### <span data-ttu-id="385aa-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="385aa-111">-Account</span></span>
<span data-ttu-id="385aa-112">Das Data Lake Store-Konto zum Aktualisieren der virtuellen Netzwerkregel in</span><span class="sxs-lookup"><span data-stu-id="385aa-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="385aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="385aa-113">-DefaultProfile</span></span>
<span data-ttu-id="385aa-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="385aa-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="385aa-115">-Name</span><span class="sxs-lookup"><span data-stu-id="385aa-115">-Name</span></span>
<span data-ttu-id="385aa-116">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="385aa-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="385aa-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="385aa-117">-PassThru</span></span>
<span data-ttu-id="385aa-118">Gibt an, dass eine boolesche Antwort zurückgegeben werden soll, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="385aa-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="385aa-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="385aa-119">-Confirm</span></span>
<span data-ttu-id="385aa-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="385aa-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="385aa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="385aa-121">-WhatIf</span></span>
<span data-ttu-id="385aa-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="385aa-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="385aa-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="385aa-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="385aa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="385aa-124">CommonParameters</span></span>
<span data-ttu-id="385aa-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="385aa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="385aa-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="385aa-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="385aa-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="385aa-127">INPUTS</span></span>

### <span data-ttu-id="385aa-128">System. String</span><span class="sxs-lookup"><span data-stu-id="385aa-128">System.String</span></span>

## <span data-ttu-id="385aa-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="385aa-129">OUTPUTS</span></span>

### <span data-ttu-id="385aa-130">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="385aa-130">System.Boolean</span></span>

## <span data-ttu-id="385aa-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="385aa-131">NOTES</span></span>

## <span data-ttu-id="385aa-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="385aa-132">RELATED LINKS</span></span>
