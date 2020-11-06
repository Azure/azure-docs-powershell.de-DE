---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchaccountkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccountKeys.md
ms.openlocfilehash: 1f32e700cd5d0c20e041143e43755172ecf2da86
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502226"
---
# <span data-ttu-id="21371-101">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="21371-101">Get-AzureRmBatchAccountKeys</span></span>

## <span data-ttu-id="21371-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="21371-102">SYNOPSIS</span></span>
<span data-ttu-id="21371-103">Ruft die Schlüssel eines Batch Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="21371-103">Gets the keys of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21371-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="21371-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccountKeys [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21371-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="21371-105">DESCRIPTION</span></span>
<span data-ttu-id="21371-106">Das Cmdlet " **Get-AzureRmBatchAccountKeys** " Ruft die Schlüssel eines Azure-Batch Kontos im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="21371-106">The **Get-AzureRmBatchAccountKeys** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="21371-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="21371-107">EXAMPLES</span></span>

## <span data-ttu-id="21371-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="21371-108">PARAMETERS</span></span>

### <span data-ttu-id="21371-109">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="21371-109">-AccountName</span></span>
<span data-ttu-id="21371-110">Gibt den Namen des Kontos an, für das dieses Cmdlet Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="21371-110">Specifies the name of the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="21371-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21371-111">-DefaultProfile</span></span>
<span data-ttu-id="21371-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="21371-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21371-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21371-113">-ResourceGroupName</span></span>
<span data-ttu-id="21371-114">Gibt den Namen der Ressourcengruppe an, die das Konto enthält, für das dieses Cmdlet Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="21371-114">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="21371-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21371-115">CommonParameters</span></span>
<span data-ttu-id="21371-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21371-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21371-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21371-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21371-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="21371-118">INPUTS</span></span>

### <span data-ttu-id="21371-119">System. String</span><span class="sxs-lookup"><span data-stu-id="21371-119">System.String</span></span>

## <span data-ttu-id="21371-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="21371-120">OUTPUTS</span></span>

### <span data-ttu-id="21371-121">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="21371-121">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="21371-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="21371-122">NOTES</span></span>

## <span data-ttu-id="21371-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="21371-123">RELATED LINKS</span></span>

[<span data-ttu-id="21371-124">Neu – AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="21371-124">New-AzureRmBatchAccountKey</span></span>](./New-AzureRmBatchAccountKey.md)

[<span data-ttu-id="21371-125">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="21371-125">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


