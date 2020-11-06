---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9BEE5888-304D-4438-BE97-D1FE254AEE98
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchAccount.md
ms.openlocfilehash: 7f1747d838d0b81d1cfa29e98134897357f33a53
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478734"
---
# <span data-ttu-id="9bc45-101">Set-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="9bc45-101">Set-AzureRmBatchAccount</span></span>

## <span data-ttu-id="9bc45-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9bc45-102">SYNOPSIS</span></span>
<span data-ttu-id="9bc45-103">Aktualisiert ein Stapelverarbeitungs Konto.</span><span class="sxs-lookup"><span data-stu-id="9bc45-103">Updates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bc45-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9bc45-104">SYNTAX</span></span>

```
Set-AzureRmBatchAccount [-AccountName] <String> [-Tag] <Hashtable> [-ResourceGroupName <String>]
 [-AutoStorageAccountId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bc45-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9bc45-105">DESCRIPTION</span></span>
<span data-ttu-id="9bc45-106">Das Cmdlet " **Satz-AzureRmBatchAccount** " aktualisiert ein Azure-Batch Konto.</span><span class="sxs-lookup"><span data-stu-id="9bc45-106">The **Set-AzureRmBatchAccount** cmdlet updates an Azure Batch account.</span></span>
<span data-ttu-id="9bc45-107">Derzeit kann dieses Cmdlet nur Tags aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="9bc45-107">Currently, this cmdlet can update only tags.</span></span>

## <span data-ttu-id="9bc45-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9bc45-108">EXAMPLES</span></span>

### <span data-ttu-id="9bc45-109">Beispiel 1: Aktualisieren der Tags in einem Stapelverarbeitungs Konto</span><span class="sxs-lookup"><span data-stu-id="9bc45-109">Example 1: Update the tags on a Batch account</span></span>
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

<span data-ttu-id="9bc45-110">Mit diesem Befehl werden die Tags für das Konto mit dem Namen pfuller aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9bc45-110">This command updates the tags on the account named pfuller.</span></span>

## <span data-ttu-id="9bc45-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9bc45-111">PARAMETERS</span></span>

### <span data-ttu-id="9bc45-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="9bc45-112">-AccountName</span></span>
<span data-ttu-id="9bc45-113">Gibt den Namen des Batch Kontos an, das vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="9bc45-113">Specifies the name of the Batch account that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bc45-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="9bc45-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="9bc45-115">Gibt die Ressourcen-ID des speicherkontos an, das für den automatischen Speicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9bc45-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bc45-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bc45-116">-DefaultProfile</span></span>
<span data-ttu-id="9bc45-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9bc45-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9bc45-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bc45-118">-ResourceGroupName</span></span>
<span data-ttu-id="9bc45-119">Gibt die Ressourcengruppe des Kontos an, das vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="9bc45-119">Specifies the resource group of the account that this cmdlet updates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bc45-120">-Tag</span><span class="sxs-lookup"><span data-stu-id="9bc45-120">-Tag</span></span>
<span data-ttu-id="9bc45-121">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="9bc45-121">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9bc45-122">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9bc45-122">For example:</span></span>

<span data-ttu-id="9bc45-123">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="9bc45-123">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bc45-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bc45-124">CommonParameters</span></span>
<span data-ttu-id="9bc45-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bc45-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bc45-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bc45-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bc45-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9bc45-127">INPUTS</span></span>

### <span data-ttu-id="9bc45-128">Keine</span><span class="sxs-lookup"><span data-stu-id="9bc45-128">None</span></span>
<span data-ttu-id="9bc45-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="9bc45-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9bc45-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9bc45-130">OUTPUTS</span></span>

### <span data-ttu-id="9bc45-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="9bc45-131">BatchAccountContext</span></span>

## <span data-ttu-id="9bc45-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="9bc45-132">NOTES</span></span>

## <span data-ttu-id="9bc45-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9bc45-133">RELATED LINKS</span></span>

[<span data-ttu-id="9bc45-134">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="9bc45-134">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="9bc45-135">Neu – AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="9bc45-135">New-AzureRmBatchAccount</span></span>](./New-AzureRmBatchAccount.md)

[<span data-ttu-id="9bc45-136">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="9bc45-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="9bc45-137">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="9bc45-137">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
