---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
ms.openlocfilehash: 6bab9613a2b109ef0cd8d0d65bf2fb770d91eb16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664288"
---
# <span data-ttu-id="996bb-101">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="996bb-101">Get-AzureRmBatchAccountKeys</span></span>

## <span data-ttu-id="996bb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="996bb-102">SYNOPSIS</span></span>
<span data-ttu-id="996bb-103">Ruft die Schlüssel eines Batch Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="996bb-103">Gets the keys of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="996bb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="996bb-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccountKeys [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="996bb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="996bb-105">DESCRIPTION</span></span>
<span data-ttu-id="996bb-106">Das Cmdlet " **Get-AzureRmBatchAccountKeys** " Ruft die Schlüssel eines Azure-Batch Kontos im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="996bb-106">The **Get-AzureRmBatchAccountKeys** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="996bb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="996bb-107">EXAMPLES</span></span>

## <span data-ttu-id="996bb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="996bb-108">PARAMETERS</span></span>

### <span data-ttu-id="996bb-109">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="996bb-109">-AccountName</span></span>
<span data-ttu-id="996bb-110">Gibt den Namen des Kontos an, für das dieses Cmdlet Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="996bb-110">Specifies the name of the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="996bb-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="996bb-111">-ResourceGroupName</span></span>
<span data-ttu-id="996bb-112">Gibt den Namen der Ressourcengruppe an, die das Konto enthält, für das dieses Cmdlet Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="996bb-112">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="996bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="996bb-113">-DefaultProfile</span></span>
<span data-ttu-id="996bb-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="996bb-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="996bb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="996bb-115">CommonParameters</span></span>
<span data-ttu-id="996bb-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="996bb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="996bb-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="996bb-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="996bb-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="996bb-118">INPUTS</span></span>

## <span data-ttu-id="996bb-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="996bb-119">OUTPUTS</span></span>

### <span data-ttu-id="996bb-120">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="996bb-120">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="996bb-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="996bb-121">NOTES</span></span>

## <span data-ttu-id="996bb-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="996bb-122">RELATED LINKS</span></span>

[<span data-ttu-id="996bb-123">Neu – AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="996bb-123">New-AzureRmBatchAccountKey</span></span>](./New-AzureRmBatchAccountKey.md)

[<span data-ttu-id="996bb-124">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="996bb-124">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


