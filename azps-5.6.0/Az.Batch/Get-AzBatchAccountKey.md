---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
ms.openlocfilehash: 07671d3318e599c9b63c4981df1ceac63178bb35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944291"
---
# <span data-ttu-id="3dd79-101">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3dd79-101">Get-AzBatchAccountKey</span></span>

## <span data-ttu-id="3dd79-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3dd79-102">SYNOPSIS</span></span>
<span data-ttu-id="3dd79-103">Ruft die Schlüssel eines Batchkontos ab.</span><span class="sxs-lookup"><span data-stu-id="3dd79-103">Gets the keys of a Batch account.</span></span>

## <span data-ttu-id="3dd79-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3dd79-104">SYNTAX</span></span>

```
Get-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3dd79-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3dd79-105">DESCRIPTION</span></span>
<span data-ttu-id="3dd79-106">Das **Get-AzBatchAccountKey-Cmdlet** ruft die Schlüssel eines Azure Batch-Kontos im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="3dd79-106">The **Get-AzBatchAccountKey** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="3dd79-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3dd79-107">EXAMPLES</span></span>

### <span data-ttu-id="3dd79-108">Beispiel 1: Holen Sie sich Batchkontoschlüssel, und speichern Sie sie in $Context Variablen für die spätere Verwendung.</span><span class="sxs-lookup"><span data-stu-id="3dd79-108">Example 1: Get batch account keys and save it in $Context variable for use later</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
```

<span data-ttu-id="3dd79-109">Dieser Befehl ruft die Kontodetails ab und speichert sie in einem `$Context` -Objekt zur späteren Verwendung.</span><span class="sxs-lookup"><span data-stu-id="3dd79-109">This command gets the account details and stores it in a `$Context` object for use later.</span></span>

### <span data-ttu-id="3dd79-110">Beispiel 2: Batchkontoschlüssel erhalten und anzeigen</span><span class="sxs-lookup"><span data-stu-id="3dd79-110">Example 2: Get batch account keys and display them</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
PS C:\>$Context.PrimaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
PS C:\>$Context.SecondaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
```

<span data-ttu-id="3dd79-111">Dieser Befehl ruft die Kontoschlüssel ab und druckt sie auf die Konsole.</span><span class="sxs-lookup"><span data-stu-id="3dd79-111">This command gets the account keys and prints them to the console.</span></span>

## <span data-ttu-id="3dd79-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3dd79-112">PARAMETERS</span></span>

### <span data-ttu-id="3dd79-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="3dd79-113">-AccountName</span></span>
<span data-ttu-id="3dd79-114">Gibt den Namen des Kontos an, für das dieses Cmdlet Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="3dd79-114">Specifies the name of the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="3dd79-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dd79-115">-DefaultProfile</span></span>
<span data-ttu-id="3dd79-116">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3dd79-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3dd79-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dd79-117">-ResourceGroupName</span></span>
<span data-ttu-id="3dd79-118">Gibt den Namen der Ressourcengruppe an, die das Konto enthält, für das dieses Cmdlet Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="3dd79-118">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="3dd79-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dd79-119">CommonParameters</span></span>
<span data-ttu-id="3dd79-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3dd79-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dd79-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3dd79-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dd79-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3dd79-122">INPUTS</span></span>

### <span data-ttu-id="3dd79-123">System.String</span><span class="sxs-lookup"><span data-stu-id="3dd79-123">System.String</span></span>

## <span data-ttu-id="3dd79-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3dd79-124">OUTPUTS</span></span>

### <span data-ttu-id="3dd79-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3dd79-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3dd79-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3dd79-126">NOTES</span></span>

## <span data-ttu-id="3dd79-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3dd79-127">RELATED LINKS</span></span>

[<span data-ttu-id="3dd79-128">New-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="3dd79-128">New-AzBatchAccountKey</span></span>](./New-AzBatchAccountKey.md)

[<span data-ttu-id="3dd79-129">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3dd79-129">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
