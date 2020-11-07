---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 5b269eef98072a7daaaf21aa0160167bb714c77a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658887"
---
# <span data-ttu-id="341bc-101">Get-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="341bc-101">Get-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="341bc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="341bc-102">SYNOPSIS</span></span>
<span data-ttu-id="341bc-103">Abrufen der NetWorkRule-Eigenschaft eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="341bc-103">Get the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="341bc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="341bc-104">SYNTAX</span></span>

```
Get-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="341bc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="341bc-105">DESCRIPTION</span></span>
<span data-ttu-id="341bc-106">Das Cmdlet " **Get-AzStorageAccountNetworkRuleSet** " Ruft die NetworkRule-Eigenschaft eines speicherkontos ab.</span><span class="sxs-lookup"><span data-stu-id="341bc-106">The **Get-AzStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="341bc-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="341bc-107">EXAMPLES</span></span>

### <span data-ttu-id="341bc-108">Beispiel 1: Abrufen der NetworkRule-Eigenschaft eines angegebenen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="341bc-108">Example 1: Get NetworkRule property of a specified Storage account</span></span>
```
PS C:\> Get-AzStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="341bc-109">Dieser Befehl ruft die NetworkRule-Eigenschaft eines angegebenen speicherkontos ab.</span><span class="sxs-lookup"><span data-stu-id="341bc-109">This command gets NetworkRule property of a specified Storage account</span></span>

## <span data-ttu-id="341bc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="341bc-110">PARAMETERS</span></span>

### <span data-ttu-id="341bc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="341bc-111">-DefaultProfile</span></span>
<span data-ttu-id="341bc-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="341bc-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="341bc-113">-Name</span><span class="sxs-lookup"><span data-stu-id="341bc-113">-Name</span></span>
<span data-ttu-id="341bc-114">Gibt den Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="341bc-114">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="341bc-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="341bc-115">-ResourceGroupName</span></span>
<span data-ttu-id="341bc-116">Gibt den Namen der Ressourcengruppe mit dem Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="341bc-116">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="341bc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="341bc-117">CommonParameters</span></span>
<span data-ttu-id="341bc-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="341bc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="341bc-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="341bc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="341bc-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="341bc-120">INPUTS</span></span>

### <span data-ttu-id="341bc-121">System. String</span><span class="sxs-lookup"><span data-stu-id="341bc-121">System.String</span></span>

## <span data-ttu-id="341bc-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="341bc-122">OUTPUTS</span></span>

### <span data-ttu-id="341bc-123">Microsoft. Azure. Commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="341bc-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="341bc-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="341bc-124">NOTES</span></span>

## <span data-ttu-id="341bc-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="341bc-125">RELATED LINKS</span></span>
