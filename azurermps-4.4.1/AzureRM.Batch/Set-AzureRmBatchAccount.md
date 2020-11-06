---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchAccount.md
ms.openlocfilehash: fbf1911f7ec0483509c8a4e93f326f17c47d7f01
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500934"
---
# <span data-ttu-id="5404f-101">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="5404f-101">Set-AzureRmBatchAccount</span></span>

## <span data-ttu-id="5404f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5404f-102">SYNOPSIS</span></span>
<span data-ttu-id="5404f-103">Aktualisiert ein Stapelverarbeitungs Konto.</span><span class="sxs-lookup"><span data-stu-id="5404f-103">Updates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5404f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5404f-104">SYNTAX</span></span>

```
Set-AzureRmBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5404f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5404f-105">DESCRIPTION</span></span>
<span data-ttu-id="5404f-106">Das Cmdlet " **Satz-AzureRmBatchAccount** " aktualisiert ein Azure-Batch Konto.</span><span class="sxs-lookup"><span data-stu-id="5404f-106">The **Set-AzureRmBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="5404f-107">Derzeit kann dieses Cmdlet nur Tags aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="5404f-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="5404f-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5404f-108">EXAMPLES</span></span>

### <span data-ttu-id="5404f-109">Beispiel 1: Aktualisieren der Tags in einem Stapelverarbeitungs Konto</span><span class="sxs-lookup"><span data-stu-id="5404f-109">Example 1: Update the tags on a Batch account</span></span>
```
PS C:\>Set-AzureRmBatchAccount -AccountName "cmdletexample" -Tag @{key0="value0";key1=$null;key2="value2"}
AccountName                  : cmdletexample
Location                     : westus
ResourceGroupName            : CmdletExampleRG
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
                               Name  Value
                               ====  ======
                               key0  value0
                               key1
                               key2  value2
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="5404f-110">Mit diesem Befehl werden die Tags für das Konto mit dem Namen pfuller aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5404f-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="5404f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="5404f-111">PARAMETERS</span></span>

### <span data-ttu-id="5404f-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="5404f-112">-AccountName</span></span>
<span data-ttu-id="5404f-113">Gibt den Namen des Batch Kontos an, das vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="5404f-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="5404f-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="5404f-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="5404f-115">Gibt die Ressourcen-ID des speicherkontos an, das für den automatischen Speicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5404f-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="5404f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5404f-116">-ResourceGroupName</span></span>
<span data-ttu-id="5404f-117">Gibt die Ressourcengruppe des Kontos an, das vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="5404f-117">Specifies the resource group of the account that this cmdlet updates.</span></span>

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

### <span data-ttu-id="5404f-118">-Tag</span><span class="sxs-lookup"><span data-stu-id="5404f-118">-Tag</span></span>
<span data-ttu-id="5404f-119">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="5404f-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5404f-120">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="5404f-120">For example:</span></span>

<span data-ttu-id="5404f-121">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="5404f-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5404f-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5404f-122">-DefaultProfile</span></span>
<span data-ttu-id="5404f-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5404f-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5404f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5404f-124">CommonParameters</span></span>
<span data-ttu-id="5404f-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5404f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5404f-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5404f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5404f-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5404f-127">INPUTS</span></span>

## <span data-ttu-id="5404f-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5404f-128">OUTPUTS</span></span>

### <span data-ttu-id="5404f-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5404f-129">BatchAccountContext</span></span>

## <span data-ttu-id="5404f-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="5404f-130">NOTES</span></span>

## <span data-ttu-id="5404f-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5404f-131">RELATED LINKS</span></span>

[<span data-ttu-id="5404f-132">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="5404f-132">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="5404f-133">Neu – AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="5404f-133">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="5404f-134">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="5404f-134">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="5404f-135">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="5404f-135">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
