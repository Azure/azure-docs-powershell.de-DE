---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: e9ce7a0ab98251b86990db5623b91b3a62a4cdcc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304256"
---
# <span data-ttu-id="64af3-101">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="64af3-101">Get-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="64af3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64af3-102">SYNOPSIS</span></span>
<span data-ttu-id="64af3-103">Die "NetWorkRule"-Eigenschaft eines Speicherkontos erhalten</span><span class="sxs-lookup"><span data-stu-id="64af3-103">Get the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="64af3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="64af3-104">SYNTAX</span></span>

```
Get-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64af3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="64af3-105">DESCRIPTION</span></span>
<span data-ttu-id="64af3-106">Das **Cmdlet "Get-AzStorageAccountNetworkRuleSet"** ruft die "NetworkRule"-Eigenschaft eines Speicherkontos ab.</span><span class="sxs-lookup"><span data-stu-id="64af3-106">The **Get-AzStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="64af3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="64af3-107">EXAMPLES</span></span>

### <span data-ttu-id="64af3-108">Beispiel 1: "Get NetworkRule"-Eigenschaft eines angegebenen Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="64af3-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="64af3-109">Dieser Befehl ruft die Eigenschaft "NetworkRule" eines angegebenen Speicherkontos ab.</span><span class="sxs-lookup"><span data-stu-id="64af3-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="64af3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64af3-110">PARAMETERS</span></span>

### <span data-ttu-id="64af3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64af3-111">-DefaultProfile</span></span>
<span data-ttu-id="64af3-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="64af3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64af3-113">-Name</span><span class="sxs-lookup"><span data-stu-id="64af3-113">-Name</span></span>
<span data-ttu-id="64af3-114">Gibt den Namen des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="64af3-114">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64af3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64af3-115">-ResourceGroupName</span></span>
<span data-ttu-id="64af3-116">Gibt den Namen der Ressourcengruppe an, die das Konto "Speicher" enthält.</span><span class="sxs-lookup"><span data-stu-id="64af3-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="64af3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64af3-117">CommonParameters</span></span>
<span data-ttu-id="64af3-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64af3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64af3-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64af3-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64af3-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="64af3-120">INPUTS</span></span>

### <span data-ttu-id="64af3-121">System.String</span><span class="sxs-lookup"><span data-stu-id="64af3-121">System.String</span></span>

## <span data-ttu-id="64af3-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="64af3-122">OUTPUTS</span></span>

### <span data-ttu-id="64af3-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="64af3-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="64af3-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="64af3-124">NOTES</span></span>

## <span data-ttu-id="64af3-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="64af3-125">RELATED LINKS</span></span>
