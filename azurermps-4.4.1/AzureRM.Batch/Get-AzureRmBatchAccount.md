---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 818D5D85-B6D5-458C-A26E-E4DE8E111A10
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchAccount.md
ms.openlocfilehash: 06d4632d9e7977639c708e81d4613b200189a2a4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502770"
---
# <span data-ttu-id="3e214-101">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3e214-101">Get-AzureRmBatchAccount</span></span>

## <span data-ttu-id="3e214-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3e214-102">SYNOPSIS</span></span>
<span data-ttu-id="3e214-103">Ruft ein Batch Konto im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="3e214-103">Gets a Batch account in the current subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e214-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e214-104">SYNTAX</span></span>

```
Get-AzureRmBatchAccount [[-AccountName] <String>] [[-ResourceGroupName] <String>] [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3e214-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e214-105">DESCRIPTION</span></span>
<span data-ttu-id="3e214-106">Das Cmdlet " **Get-AzureRmBatchAccount** " ruft im aktuellen Abonnement ein Azure-Batch Konto ab.</span><span class="sxs-lookup"><span data-stu-id="3e214-106">The **Get-AzureRmBatchAccount** cmdlet gets an Azure Batch account in the current subscription.</span></span> <span data-ttu-id="3e214-107">Sie können den *Konto* -Parameter verwenden, um ein einzelnes Konto zu erhalten, oder Sie können den *ResourceGroupName* -Parameter verwenden, um Konten unter dieser Ressourcengruppe abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3e214-107">You can use the *AccountName* parameter to get a single account, or you can use the *ResourceGroupName* parameter to get accounts under that resource group.</span></span>

## <span data-ttu-id="3e214-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e214-108">EXAMPLES</span></span>

### <span data-ttu-id="3e214-109">Beispiel 1: Abrufen eines Batch Kontos nach Name</span><span class="sxs-lookup"><span data-stu-id="3e214-109">Example 1: Get a batch account by name</span></span>
```
PS C:\>Get-AzureRmBatchAccount -AccountName "pfuller"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://pfuller.westus.batch.azure.com
```

<span data-ttu-id="3e214-110">Dieser Befehl ruft das Batch Konto mit dem Namen pfuller ab.</span><span class="sxs-lookup"><span data-stu-id="3e214-110">This command gets the batch account named pfuller.</span></span>

### <span data-ttu-id="3e214-111">Beispiel 2: Abrufen der einer Ressourcengruppe zugeordneten Stapelverarbeitungs Konten</span><span class="sxs-lookup"><span data-stu-id="3e214-111">Example 2: Get the batch accounts associated with a resource group</span></span>
```
PS C:\>Get-AzureRmBatchAccount -ResourceGroupName "CmdletExampleRG"
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
AccountName                  : cmdletexample2
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="3e214-112">Dieser Befehl ruft die Stapelverarbeitungs Konten ab, die der CmdletExampleRG-Ressourcengruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="3e214-112">This command gets the batch accounts associated with the CmdletExampleRG resource group.</span></span>

## <span data-ttu-id="3e214-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e214-113">PARAMETERS</span></span>

### <span data-ttu-id="3e214-114">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="3e214-114">-AccountName</span></span>
<span data-ttu-id="3e214-115">Gibt den Namen eines Kontos an.</span><span class="sxs-lookup"><span data-stu-id="3e214-115">Specifies the name of an account.</span></span>
<span data-ttu-id="3e214-116">Wenn Sie einen Kontonamen angeben, gibt dieses Cmdlet nur dieses Konto zurück.</span><span class="sxs-lookup"><span data-stu-id="3e214-116">If you specify an account name, this cmdlet only returns that account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e214-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e214-117">-ResourceGroupName</span></span>
<span data-ttu-id="3e214-118">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3e214-118">Specifies the name of a resource group.</span></span>
<span data-ttu-id="3e214-119">Wenn Sie eine Ressourcengruppe angeben, ruft dieses Cmdlet die Konten unter der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="3e214-119">If you specify a resource group, this cmdlet gets the accounts under the specified resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e214-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="3e214-120">-Tag</span></span>
<span data-ttu-id="3e214-121">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="3e214-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3e214-122">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3e214-122">For example:</span></span>

<span data-ttu-id="3e214-123">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="3e214-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

<span data-ttu-id="3e214-124">Dieses Cmdlet ruft Konten ab, die die Tags enthalten, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="3e214-124">This cmdlet gets accounts that contain the tags that this parameter specifies.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e214-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e214-125">-DefaultProfile</span></span>
<span data-ttu-id="3e214-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3e214-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e214-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e214-127">CommonParameters</span></span>
<span data-ttu-id="3e214-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e214-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e214-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e214-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e214-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3e214-130">INPUTS</span></span>

## <span data-ttu-id="3e214-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3e214-131">OUTPUTS</span></span>

### <span data-ttu-id="3e214-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="3e214-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="3e214-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="3e214-133">NOTES</span></span>

## <span data-ttu-id="3e214-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3e214-134">RELATED LINKS</span></span>

[<span data-ttu-id="3e214-135">Neu – AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3e214-135">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="3e214-136">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3e214-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="3e214-137">Satz-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="3e214-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="3e214-138">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="3e214-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
