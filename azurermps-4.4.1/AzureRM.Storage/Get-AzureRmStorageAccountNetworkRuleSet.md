---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 00447be14fe61b76a4dbb4f62e3393bb76c1ddb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665235"
---
# <span data-ttu-id="1018c-101">Get-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1018c-101">Get-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="1018c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1018c-102">SYNOPSIS</span></span>
<span data-ttu-id="1018c-103">Abrufen der NetWorkRule-Eigenschaft eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="1018c-103">Get the NetWorkRule property of a Storage Account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1018c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1018c-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1018c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1018c-105">DESCRIPTION</span></span>
<span data-ttu-id="1018c-106">Das Cmdlet " **Get-AzureRmStorageAccountNetworkRuleSet** " Ruft die NetworkRule-Eigenschaft eines speicherkontos ab.</span><span class="sxs-lookup"><span data-stu-id="1018c-106">The **Get-AzureRmStorageAccountNetworkRuleSet** cmdlet gets the NetworkRule property of a Storage Account</span></span>

## <span data-ttu-id="1018c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1018c-107">EXAMPLES</span></span>

### <span data-ttu-id="1018c-108">Beispiel 1: Abrufen der NetworkRule-Eigenschaft eines angegebenen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="1018c-108">Example 1: Get NetworkRule property of a specified storage account</span></span>
```
PS C:\> Get-AzureRmStorageAccountNetworkRuleSet  -ResourceGroupName "rg1" -AccountName "mystorageaccount"
```

<span data-ttu-id="1018c-109">Dieser Befehl ruft die NetworkRule-Eigenschaft eines angegebenen speicherkontos ab.</span><span class="sxs-lookup"><span data-stu-id="1018c-109">This command gets NetworkRule property of a specified storage account</span></span>

## <span data-ttu-id="1018c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1018c-110">PARAMETERS</span></span>

### <span data-ttu-id="1018c-111">-Name</span><span class="sxs-lookup"><span data-stu-id="1018c-111">-Name</span></span>
<span data-ttu-id="1018c-112">Gibt den Namen des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="1018c-112">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="1018c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1018c-113">-ResourceGroupName</span></span>
<span data-ttu-id="1018c-114">Gibt den Namen der Ressourcengruppe mit dem Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="1018c-114">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="1018c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1018c-115">-DefaultProfile</span></span>
<span data-ttu-id="1018c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1018c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1018c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1018c-117">CommonParameters</span></span>
<span data-ttu-id="1018c-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1018c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1018c-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1018c-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1018c-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1018c-120">INPUTS</span></span>

### <span data-ttu-id="1018c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="1018c-121">System.String</span></span>

## <span data-ttu-id="1018c-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1018c-122">OUTPUTS</span></span>

### <span data-ttu-id="1018c-123">Microsoft. Azure. Commands. Management. Storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="1018c-123">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="1018c-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="1018c-124">NOTES</span></span>

## <span data-ttu-id="1018c-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1018c-125">RELATED LINKS</span></span>

