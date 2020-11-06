---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 486748AC-3932-4E0C-BBCC-2BC194E69DCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccountKey.md
ms.openlocfilehash: 48de3ae521f77c531433ffca67dadc9e2c46a980
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502225"
---
# <span data-ttu-id="28c06-101">New-AzureRmBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="28c06-101">New-AzureRmBatchAccountKey</span></span>

## <span data-ttu-id="28c06-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="28c06-102">SYNOPSIS</span></span>
<span data-ttu-id="28c06-103">Generiert einen Schlüssel eines Batch Kontos erneut.</span><span class="sxs-lookup"><span data-stu-id="28c06-103">Regenerates a key of a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28c06-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="28c06-104">SYNTAX</span></span>

```
New-AzureRmBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>] -KeyType <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28c06-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28c06-105">DESCRIPTION</span></span>
<span data-ttu-id="28c06-106">Das Cmdlet **New-AzureRmBatchAccountKey** generiert den primären oder sekundären Schlüssel eines Azure-Batch Kontos erneut.</span><span class="sxs-lookup"><span data-stu-id="28c06-106">The **New-AzureRmBatchAccountKey** cmdlet regenerates the primary or secondary key of an Azure Batch account.</span></span>
<span data-ttu-id="28c06-107">Das Cmdlet gibt ein **BatchAccountContext** -Objekt zurück, das die aktuellen **PrimaryAccountKey** -und **SecondaryAccountKey** -Eigenschaften aufweist.</span><span class="sxs-lookup"><span data-stu-id="28c06-107">The cmdlet returns a **BatchAccountContext** object that has its current **PrimaryAccountKey** and **SecondaryAccountKey** properties.</span></span>

## <span data-ttu-id="28c06-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28c06-108">EXAMPLES</span></span>

### <span data-ttu-id="28c06-109">Beispiel 1: Erneutes Generieren des primär kontoschlüssels für ein Stapelverarbeitungs Konto</span><span class="sxs-lookup"><span data-stu-id="28c06-109">Example 1: Regenerate the primary account key on a Batch account</span></span>
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

<span data-ttu-id="28c06-110">Mit diesem Befehl wird der primäre Kontoschlüssel für das Batch Konto mit dem Namen pfuller erneut generiert.</span><span class="sxs-lookup"><span data-stu-id="28c06-110">This command regenerates the primary account key on the Batch account named pfuller.</span></span>

## <span data-ttu-id="28c06-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="28c06-111">PARAMETERS</span></span>

### <span data-ttu-id="28c06-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="28c06-112">-AccountName</span></span>
<span data-ttu-id="28c06-113">Gibt den Namen des Batch Kontos an, für das dieses Cmdlet einen Schlüssel neu generiert.</span><span class="sxs-lookup"><span data-stu-id="28c06-113">Specifies the name of the Batch account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="28c06-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28c06-114">-DefaultProfile</span></span>
<span data-ttu-id="28c06-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="28c06-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28c06-116">-KeyType</span><span class="sxs-lookup"><span data-stu-id="28c06-116">-KeyType</span></span>
<span data-ttu-id="28c06-117">Gibt den Typ des Schlüssels an, der vom Cmdlet neu generiert wird.</span><span class="sxs-lookup"><span data-stu-id="28c06-117">Specifies the type of key that this cmdlet regenerates.</span></span>
<span data-ttu-id="28c06-118">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="28c06-118">Valid values are:</span></span> 
- <span data-ttu-id="28c06-119">Primär</span><span class="sxs-lookup"><span data-stu-id="28c06-119">Primary</span></span>
- <span data-ttu-id="28c06-120">Sekundär</span><span class="sxs-lookup"><span data-stu-id="28c06-120">Secondary</span></span>

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

### <span data-ttu-id="28c06-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28c06-121">-ResourceGroupName</span></span>
<span data-ttu-id="28c06-122">Gibt die Ressourcengruppe des Kontos an, für das dieses Cmdlet einen Schlüssel neu generiert.</span><span class="sxs-lookup"><span data-stu-id="28c06-122">Specifies the resource group of the account for which this cmdlet regenerates a key.</span></span>

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

### <span data-ttu-id="28c06-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28c06-123">CommonParameters</span></span>
<span data-ttu-id="28c06-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28c06-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28c06-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28c06-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28c06-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="28c06-126">INPUTS</span></span>

### <span data-ttu-id="28c06-127">System. String</span><span class="sxs-lookup"><span data-stu-id="28c06-127">System.String</span></span>

## <span data-ttu-id="28c06-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="28c06-128">OUTPUTS</span></span>

### <span data-ttu-id="28c06-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="28c06-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="28c06-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="28c06-130">NOTES</span></span>

## <span data-ttu-id="28c06-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="28c06-131">RELATED LINKS</span></span>

[<span data-ttu-id="28c06-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="28c06-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="28c06-133">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="28c06-133">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


