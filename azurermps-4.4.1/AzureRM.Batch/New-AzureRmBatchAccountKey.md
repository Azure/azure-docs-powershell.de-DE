---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
ms.openlocfilehash: fbfcbaa0fdf790daad05aece6190396c735f9fff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662978"
---
# <span data-ttu-id="ba4b8-101">New-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="ba4b8-101">New-AzureRmBatchAccountKey</span></span>

## <span data-ttu-id="ba4b8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ba4b8-102">SYNOPSIS</span></span>
<span data-ttu-id="ba4b8-103">Generiert einen Schlüssel eines Batch Kontos erneut.</span><span class="sxs-lookup"><span data-stu-id="ba4b8-103">Regenerates a key of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ba4b8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ba4b8-104">SYNTAX</span></span>

```
New-AzureRmBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ba4b8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ba4b8-105">DESCRIPTION</span></span>
<span data-ttu-id="ba4b8-106">Das Cmdlet **New-AzureRmBatchAccountKey** generiert den primären oder sekundären Schlüssel eines Azure-Batch Kontos erneut.</span><span class="sxs-lookup"><span data-stu-id="ba4b8-106">The **New-AzureRmBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="ba4b8-107">Das Cmdlet gibt ein **BatchAccountContext** -Objekt zurück, das die aktuellen **PrimaryAccountKey** -und **SecondaryAccountKey** -Eigenschaften aufweist.</span><span class="sxs-lookup"><span data-stu-id="ba4b8-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="ba4b8-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ba4b8-108">EXAMPLES</span></span>

### <span data-ttu-id="ba4b8-109">Beispiel 1: Erneutes Generieren des primär kontoschlüssels für ein Stapelverarbeitungs Konto</span><span class="sxs-lookup"><span data-stu-id="ba4b8-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
```
PS C:\>New-AzureRmBatchAccountKey -AccountName "pfuller" -KeyType "Primary"
AccountName                  : pfuller

Location                     : westus

ResourceGroupName            : CmdletExampleRG

CoreQuota                    : 20

PoolQuota                    : 20

ActiveJobAndJobScheduleQuota : 20

Tags                         : 
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="ba4b8-110">Mit diesem Befehl wird der primäre Kontoschlüssel für das Batch Konto mit dem Namen pfuller erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="ba4b8-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="ba4b8-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ba4b8-111">PARAMETERS</span></span>

### <span data-ttu-id="ba4b8-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="ba4b8-112">-AccountName</span></span>
<span data-ttu-id="ba4b8-113">Gibt den Namen des Batch Kontos an, für das dieses Cmdlet einen Schlüssel neu generiert.</span><span class="sxs-lookup"><span data-stu-id="ba4b8-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="ba4b8-114">-KeyType</span><span class="sxs-lookup"><span data-stu-id="ba4b8-114">-KeyType</span></span>
<span data-ttu-id="ba4b8-115">Gibt den Typ des Schlüssels an, der vom Cmdlet neu generiert wird.</span><span class="sxs-lookup"><span data-stu-id="ba4b8-115">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="ba4b8-116">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="ba4b8-116">Valid values are:</span></span> 

- <span data-ttu-id="ba4b8-117">Primär</span><span class="sxs-lookup"><span data-stu-id="ba4b8-117">Primary</span></span>
- <span data-ttu-id="ba4b8-118">Sekundär</span><span class="sxs-lookup"><span data-stu-id="ba4b8-118">Secondary</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba4b8-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba4b8-119">-ResourceGroupName</span></span>
<span data-ttu-id="ba4b8-120">Gibt die Ressourcengruppe des Kontos an, für das dieses Cmdlet einen Schlüssel neu generiert.</span><span class="sxs-lookup"><span data-stu-id="ba4b8-120">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="ba4b8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba4b8-121">-DefaultProfile</span></span>
<span data-ttu-id="ba4b8-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ba4b8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba4b8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba4b8-123">CommonParameters</span></span>
<span data-ttu-id="ba4b8-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba4b8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba4b8-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba4b8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba4b8-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ba4b8-126">INPUTS</span></span>

## <span data-ttu-id="ba4b8-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ba4b8-127">OUTPUTS</span></span>

### <span data-ttu-id="ba4b8-128">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="ba4b8-128">BatchAccountContext</span></span>

## <span data-ttu-id="ba4b8-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="ba4b8-129">NOTES</span></span>

## <span data-ttu-id="ba4b8-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ba4b8-130">RELATED LINKS</span></span>

[<span data-ttu-id="ba4b8-131">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="ba4b8-131">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="ba4b8-132">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="ba4b8-132">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


