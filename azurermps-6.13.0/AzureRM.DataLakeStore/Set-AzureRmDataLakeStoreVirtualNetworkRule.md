---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/set-azurermdatalakestorevirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Set-AzureRmDataLakeStoreVirtualNetworkRule.md
ms.openlocfilehash: b05158ae21219760c9c88fe9c0ae3e4978b76f33
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482502"
---
# <span data-ttu-id="da980-101">Set-AzureRmDataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="da980-101">Set-AzureRmDataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="da980-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="da980-102">SYNOPSIS</span></span>
<span data-ttu-id="da980-103">Ändert die angegebene virtuelle Netzwerkregel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="da980-103">Modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="da980-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="da980-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeStoreVirtualNetworkRule [-Account] <String> [-Name] <String> [-SubnetId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="da980-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="da980-105">DESCRIPTION</span></span>
<span data-ttu-id="da980-106">Das Cmdlet " **Satz-AzureRmDataLakeStoreVirtualNetworkRule** " ändert die angegebene virtuelle Netzwerkregel im angegebenen Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="da980-106">The **Set-AzureRmDataLakeStoreVirtualNetworkRule** cmdlet modifies the specified virtual network rule in the specified Data Lake Store.</span></span>

## <span data-ttu-id="da980-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="da980-107">EXAMPLES</span></span>

### <span data-ttu-id="da980-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="da980-108">Example 1</span></span>
```powershell
PS C:\> Set-AzureRmDataLakeStoreVirtualNetworkRule -Account "dls" -Name "myVNET" -SubnetId "updatedId"

ResourceGroupName                :
AccountName                      :
VirtualNetworkRuleName           : myVNET
VirtualNetworkSubnetId           : /subscriptions/<subscriptionId>/resourceGroups/<resourceGroup>/providers/Microsoft.Network/virtualNetworks/myVNET/subnets/updatedId
IgnoreMissingVnetServiceEndpoint :
State                            :
```

<span data-ttu-id="da980-109">Aktualisiert die Subnetz-ID der virtuellen Netzwerkregel "myVNET" in Konto "DLS" auf "aktualisiert".</span><span class="sxs-lookup"><span data-stu-id="da980-109">Updates the subnet id of virtual network rule "myVNET" in account "dls" to "updatedId"</span></span>

## <span data-ttu-id="da980-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="da980-110">PARAMETERS</span></span>

### <span data-ttu-id="da980-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="da980-111">-Account</span></span>
<span data-ttu-id="da980-112">Das Data Lake Store-Konto zum Aktualisieren der virtuellen Netzwerkregel in</span><span class="sxs-lookup"><span data-stu-id="da980-112">The Data Lake Store account to update the virtual network rule in</span></span>

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

### <span data-ttu-id="da980-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da980-113">-DefaultProfile</span></span>
<span data-ttu-id="da980-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="da980-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="da980-115">-Name</span><span class="sxs-lookup"><span data-stu-id="da980-115">-Name</span></span>
<span data-ttu-id="da980-116">Der Name der Regel für das virtuelle Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="da980-116">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="da980-117">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="da980-117">-SubnetId</span></span>
<span data-ttu-id="da980-118">Der Anfang des gültigen IP-Bereichs für die Regel "virtuelles Netzwerk"</span><span class="sxs-lookup"><span data-stu-id="da980-118">The start of the valid ip range for the virtual network rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="da980-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="da980-119">-Confirm</span></span>
<span data-ttu-id="da980-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="da980-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="da980-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="da980-121">-WhatIf</span></span>
<span data-ttu-id="da980-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="da980-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="da980-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="da980-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="da980-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da980-124">CommonParameters</span></span>
<span data-ttu-id="da980-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da980-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da980-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da980-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da980-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="da980-127">INPUTS</span></span>

### <span data-ttu-id="da980-128">System. String</span><span class="sxs-lookup"><span data-stu-id="da980-128">System.String</span></span>

## <span data-ttu-id="da980-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="da980-129">OUTPUTS</span></span>

### <span data-ttu-id="da980-130">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="da980-130">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreVirtualNetworkRule</span></span>

## <span data-ttu-id="da980-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="da980-131">NOTES</span></span>

## <span data-ttu-id="da980-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="da980-132">RELATED LINKS</span></span>
