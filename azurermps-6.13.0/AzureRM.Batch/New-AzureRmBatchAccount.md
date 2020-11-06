---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
ms.openlocfilehash: d634ab23912c45a0916ccf64244dda24190c6ee3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480542"
---
# <span data-ttu-id="871cf-101">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="871cf-101">New-AzureRmBatchAccount</span></span>

## <span data-ttu-id="871cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="871cf-102">SYNOPSIS</span></span>
<span data-ttu-id="871cf-103">Erstellt ein Stapelverarbeitungs Konto.</span><span class="sxs-lookup"><span data-stu-id="871cf-103">Creates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="871cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="871cf-104">SYNTAX</span></span>

```
New-AzureRmBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-PoolAllocationMode <PoolAllocationMode>] [-KeyVaultId <String>]
 [-KeyVaultUrl <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="871cf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="871cf-105">DESCRIPTION</span></span>
<span data-ttu-id="871cf-106">Das Cmdlet **New-AzureRmBatchAccount** erstellt ein Azure-Batch Konto für die angegebene Ressourcengruppe und den angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="871cf-106">The **New-AzureRmBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="871cf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="871cf-107">EXAMPLES</span></span>

### <span data-ttu-id="871cf-108">Beispiel 1: Erstellen eines Stapelverarbeitungs Kontos</span><span class="sxs-lookup"><span data-stu-id="871cf-108">Example 1: Create a Batch account</span></span>
```
PS C:\>New-AzureRmBatchAccount -AccountName "pfuller" -ResourceGroupName "ResourceGroup03" -Location "WestUS"
AccountName                  : pfuller
Location                     : westus
ResourceGroupName            : ResourceGroup03
CoreQuota                    : 20
PoolQuota                    : 20
ActiveJobAndJobScheduleQuota : 20
Tags                         :
TaskTenantUrl                : https://cmdletexample.westus.batch.azure.com
```

<span data-ttu-id="871cf-109">Mit diesem Befehl wird ein Batch Konto mit dem Namen pfuller mithilfe der ResourceGroup03-Ressourcengruppe am Standort West Amerika erstellt.</span><span class="sxs-lookup"><span data-stu-id="871cf-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="871cf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="871cf-110">PARAMETERS</span></span>

### <span data-ttu-id="871cf-111">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="871cf-111">-AccountName</span></span>
<span data-ttu-id="871cf-112">Gibt den Namen des Batch Kontos an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="871cf-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>
<span data-ttu-id="871cf-113">Stapel Kontonamen müssen zwischen 3 und 24 Zeichen lang sein und nur Zahlen und Kleinbuchstaben enthalten.</span><span class="sxs-lookup"><span data-stu-id="871cf-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

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

### <span data-ttu-id="871cf-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="871cf-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="871cf-115">Gibt die Ressourcen-ID des speicherkontos an, das für den automatischen Speicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="871cf-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="871cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="871cf-116">-DefaultProfile</span></span>
<span data-ttu-id="871cf-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="871cf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="871cf-118">-Keyvault-Nr.</span><span class="sxs-lookup"><span data-stu-id="871cf-118">-KeyVaultId</span></span>
<span data-ttu-id="871cf-119">Die Ressourcen-ID des Azure-Schlüssel Tresors, der dem Batch Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="871cf-119">The resource ID of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="871cf-120">-KeyVaultUrl</span><span class="sxs-lookup"><span data-stu-id="871cf-120">-KeyVaultUrl</span></span>
<span data-ttu-id="871cf-121">Die URL des Azure-Schlüssel Tresors, der dem Batch Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="871cf-121">The URL of the Azure key vault associated with the Batch account.</span></span>

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

### <span data-ttu-id="871cf-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="871cf-122">-Location</span></span>
<span data-ttu-id="871cf-123">Gibt den Bereich an, in dem dieses Cmdlet das Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="871cf-123">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="871cf-124">Weitere Informationen finden Sie unter [Azure-Bereiche](https://azure.microsoft.com/en-us/regions).</span><span class="sxs-lookup"><span data-stu-id="871cf-124">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="871cf-125">-PoolAllocationMode</span><span class="sxs-lookup"><span data-stu-id="871cf-125">-PoolAllocationMode</span></span>
<span data-ttu-id="871cf-126">Der Zuordnungsmodus zum Erstellen von Pools im Stapelverarbeitungs Konto.</span><span class="sxs-lookup"><span data-stu-id="871cf-126">The allocation mode for creating pools in the Batch account.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode]
Parameter Sets: (All)
Aliases:
Accepted values: BatchService, UserSubscription

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="871cf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="871cf-127">-ResourceGroupName</span></span>
<span data-ttu-id="871cf-128">Gibt den Namen der Ressourcengruppe an, in der dieses Cmdlet das Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="871cf-128">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="871cf-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="871cf-129">-Tag</span></span>
<span data-ttu-id="871cf-130">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="871cf-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="871cf-131">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="871cf-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="871cf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="871cf-132">CommonParameters</span></span>
<span data-ttu-id="871cf-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="871cf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="871cf-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="871cf-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="871cf-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="871cf-135">INPUTS</span></span>

### <span data-ttu-id="871cf-136">System. String</span><span class="sxs-lookup"><span data-stu-id="871cf-136">System.String</span></span>

### <span data-ttu-id="871cf-137">System. Nullable ' 1 [[Microsoft.Azure.Management.Batch. Models. PoolAllocationMode, Microsoft.Azure.Management.Batch, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="871cf-137">System.Nullable\`1[[Microsoft.Azure.Management.Batch.Models.PoolAllocationMode, Microsoft.Azure.Management.Batch, Version=4.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

### <span data-ttu-id="871cf-138">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="871cf-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="871cf-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="871cf-139">OUTPUTS</span></span>

### <span data-ttu-id="871cf-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="871cf-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="871cf-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="871cf-141">NOTES</span></span>

## <span data-ttu-id="871cf-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="871cf-142">RELATED LINKS</span></span>

[<span data-ttu-id="871cf-143">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="871cf-143">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="871cf-144">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="871cf-144">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="871cf-145">Satz-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="871cf-145">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="871cf-146">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="871cf-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
