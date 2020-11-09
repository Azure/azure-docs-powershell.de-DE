---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: 8fbb586e1829cd40302ab290c2d671c67666b7e3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297934"
---
# <span data-ttu-id="a2191-101">Add-AzDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a2191-101">Add-AzDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="a2191-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a2191-102">SYNOPSIS</span></span>
<span data-ttu-id="a2191-103">Fügt dem angegebenen Data Lake Store-Konto eine virtuelle Netzwerkregel hinzu.</span><span class="sxs-lookup"><span data-stu-id="a2191-103">Adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="a2191-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a2191-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a2191-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a2191-105">DESCRIPTION</span></span>
<span data-ttu-id="a2191-106">Mit dem Cmdlet **Add-AzDataLakeStoreVirtualNetworkRule** wird dem angegebenen Data Lake Store-Konto eine virtuelle Netzwerkregel hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a2191-106">The **Add-AzDataLakeStoreVirtualNetworkRule** cmdlet adds a virtual network rule to the specified Data Lake Store account.</span></span>

## <span data-ttu-id="a2191-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a2191-107">EXAMPLES</span></span>

### <span data-ttu-id="a2191-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a2191-108">Example 1</span></span>
```powershell
PS C:\> Add-AzDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "testId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/testId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="a2191-109">Dadurch wird eine neue virtuelle Netzwerkregel namens "myVNET" im Konto "DLS" mit einer Subnetzmaske "Test-ID" erstellt.</span><span class="sxs-lookup"><span data-stu-id="a2191-109">This creates a new virtual network rule called "myVNET" in account "dls" with a subnet id "testId"</span></span>

## <span data-ttu-id="a2191-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a2191-110">PARAMETERS</span></span>

### <span data-ttu-id="a2191-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="a2191-111">-Account</span></span>
<span data-ttu-id="a2191-112">Das Data Lake Store-Konto zum Hinzufügen der Regel für das virtuelle Netzwerk</span><span class="sxs-lookup"><span data-stu-id="a2191-112">The Data Lake Store account to add the virtual network rule to</span></span>

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

### <span data-ttu-id="a2191-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2191-113">-DefaultProfile</span></span>
<span data-ttu-id="a2191-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a2191-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2191-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a2191-115">-Name</span></span>
<span data-ttu-id="a2191-116">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a2191-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="a2191-117">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="a2191-117">-SubnetId</span></span>
<span data-ttu-id="a2191-118">Die Subnet-Nr der virtuellen Netzwerkregel</span><span class="sxs-lookup"><span data-stu-id="a2191-118">The subnetId of the virtual network rule</span></span>

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

### <span data-ttu-id="a2191-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a2191-119">-Confirm</span></span>
<span data-ttu-id="a2191-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a2191-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a2191-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a2191-121">-WhatIf</span></span>
<span data-ttu-id="a2191-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2191-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a2191-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a2191-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a2191-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2191-124">CommonParameters</span></span>
<span data-ttu-id="a2191-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2191-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2191-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2191-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2191-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a2191-127">INPUTS</span></span>

### <span data-ttu-id="a2191-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a2191-128">System.String</span></span>

## <span data-ttu-id="a2191-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a2191-129">OUTPUTS</span></span>

### <span data-ttu-id="a2191-130">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="a2191-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="a2191-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="a2191-131">NOTES</span></span>

## <span data-ttu-id="a2191-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a2191-132">RELATED LINKS</span></span>
