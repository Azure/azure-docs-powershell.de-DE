---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 9e455b7160b731f20e5dad6230b2015f73ca5390
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148140"
---
# <span data-ttu-id="8de11-101">Remove-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="8de11-101">Remove-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="8de11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8de11-102">SYNOPSIS</span></span>
<span data-ttu-id="8de11-103">Entfernt die angegebene Virtuelle Netzwerkregel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8de11-103">Removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="8de11-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8de11-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreVirtualNetworkRule [-Account] <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8de11-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8de11-105">DESCRIPTION</span></span>
<span data-ttu-id="8de11-106">Das **Cmdlet "Remove-AzDataLakeStoreVirtualNetworkRule"** entfernt die angegebene virtuelle Netzwerkregel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8de11-106">The **Remove-AzDataLakeStoreVirtualNetworkRule** cmdlet removes the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="8de11-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8de11-107">EXAMPLES</span></span>

### <span data-ttu-id="8de11-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8de11-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET"
```

<span data-ttu-id="8de11-109">Entfernt die Virtuelle Netzwerkregel "myVNET" aus dem Konto "dls".</span><span class="sxs-lookup"><span data-stu-id="8de11-109">Removes virtual network rule "myVNET" from account "dls"</span></span>

## <span data-ttu-id="8de11-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8de11-110">PARAMETERS</span></span>

### <span data-ttu-id="8de11-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="8de11-111">-Account</span></span>
<span data-ttu-id="8de11-112">Das Data Lake Store-Konto zum Aktualisieren der virtuellen Netzwerkregel in</span><span class="sxs-lookup"><span data-stu-id="8de11-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="8de11-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8de11-113">-DefaultProfile</span></span>
<span data-ttu-id="8de11-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8de11-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8de11-115">-Name</span><span class="sxs-lookup"><span data-stu-id="8de11-115">-Name</span></span>
<span data-ttu-id="8de11-116">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="8de11-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="8de11-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8de11-117">-PassThru</span></span>
<span data-ttu-id="8de11-118">Gibt an, dass eine boolesche Antwort zurückgegeben werden sollte, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="8de11-118">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

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

### <span data-ttu-id="8de11-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8de11-119">-Confirm</span></span>
<span data-ttu-id="8de11-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8de11-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8de11-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8de11-121">-WhatIf</span></span>
<span data-ttu-id="8de11-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8de11-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8de11-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8de11-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8de11-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de11-124">CommonParameters</span></span>
<span data-ttu-id="8de11-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8de11-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de11-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8de11-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de11-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8de11-127">INPUTS</span></span>

### <span data-ttu-id="8de11-128">System.String</span><span class="sxs-lookup"><span data-stu-id="8de11-128">System.String</span></span>

## <span data-ttu-id="8de11-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8de11-129">OUTPUTS</span></span>

### <span data-ttu-id="8de11-130">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8de11-130">System.Boolean</span></span>

## <span data-ttu-id="8de11-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8de11-131">NOTES</span></span>

## <span data-ttu-id="8de11-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8de11-132">RELATED LINKS</span></span>
