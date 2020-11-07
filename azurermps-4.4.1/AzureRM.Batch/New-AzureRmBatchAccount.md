---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 82C7B128-8818-4390-B1A5-CB40AC9D53CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchAccount.md
ms.openlocfilehash: ed44fa5960935bbe353d775a426e023512327e7f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662977"
---
# <span data-ttu-id="966e6-101">New-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="966e6-101">New-AzureRmBatchAccount</span></span>

## <span data-ttu-id="966e6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="966e6-102">SYNOPSIS</span></span>
<span data-ttu-id="966e6-103">Erstellt ein Stapelverarbeitungs Konto.</span><span class="sxs-lookup"><span data-stu-id="966e6-103">Creates a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="966e6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="966e6-104">SYNTAX</span></span>

```
New-AzureRmBatchAccount [-AccountName] <String> [-Location] <String> [-ResourceGroupName] <String>
 [[-AutoStorageAccountId] <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="966e6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="966e6-105">DESCRIPTION</span></span>
<span data-ttu-id="966e6-106">Das Cmdlet **New-AzureRmBatchAccount** erstellt ein Azure-Batch Konto für die angegebene Ressourcengruppe und den angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="966e6-106">The **New-AzureRmBatchAccount** cmdlet creates an Azure Batch account for the specified resource group and location.</span></span>

## <span data-ttu-id="966e6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="966e6-107">EXAMPLES</span></span>

### <span data-ttu-id="966e6-108">Beispiel 1: Erstellen eines Stapelverarbeitungs Kontos</span><span class="sxs-lookup"><span data-stu-id="966e6-108">Example 1: Create a Batch account</span></span>
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

<span data-ttu-id="966e6-109">Mit diesem Befehl wird ein Batch Konto mit dem Namen pfuller mithilfe der ResourceGroup03-Ressourcengruppe am Standort West Amerika erstellt.</span><span class="sxs-lookup"><span data-stu-id="966e6-109">This command creates a Batch account named pfuller using the ResourceGroup03 resource group in the West US location.</span></span>

## <span data-ttu-id="966e6-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="966e6-110">PARAMETERS</span></span>

### <span data-ttu-id="966e6-111">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="966e6-111">-AccountName</span></span>
<span data-ttu-id="966e6-112">Gibt den Namen des Batch Kontos an, das von diesem Cmdlet erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="966e6-112">Specifies the name of the Batch account that this cmdlet creates.</span></span>

<span data-ttu-id="966e6-113">Stapel Kontonamen müssen zwischen 3 und 24 Zeichen lang sein und nur Zahlen und Kleinbuchstaben enthalten.</span><span class="sxs-lookup"><span data-stu-id="966e6-113">Batch account names must be between 3 and 24 characters long and contain only numbers and lowercase letters.</span></span>

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

### <span data-ttu-id="966e6-114">-AutoStorageAccountId</span><span class="sxs-lookup"><span data-stu-id="966e6-114">-AutoStorageAccountId</span></span>
<span data-ttu-id="966e6-115">Gibt die Ressourcen-ID des speicherkontos an, das für den automatischen Speicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="966e6-115">Specifies the resource ID of the storage account to be used for auto storage.</span></span>

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

### <span data-ttu-id="966e6-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="966e6-116">-Location</span></span>
<span data-ttu-id="966e6-117">Gibt den Bereich an, in dem dieses Cmdlet das Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="966e6-117">Specifies the region where this cmdlet creates the account.</span></span>
<span data-ttu-id="966e6-118">Weitere Informationen finden Sie unter [Azure-Bereiche](https://azure.microsoft.com/en-us/regions).</span><span class="sxs-lookup"><span data-stu-id="966e6-118">For more information, see [Azure Regions](https://azure.microsoft.com/en-us/regions).</span></span>

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

### <span data-ttu-id="966e6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="966e6-119">-ResourceGroupName</span></span>
<span data-ttu-id="966e6-120">Gibt den Namen der Ressourcengruppe an, in der dieses Cmdlet das Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="966e6-120">Specifies the name of the resource group in which this cmdlet creates the account.</span></span>

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

### <span data-ttu-id="966e6-121">-Tag</span><span class="sxs-lookup"><span data-stu-id="966e6-121">-Tag</span></span>
<span data-ttu-id="966e6-122">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="966e6-122">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="966e6-123">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="966e6-123">For example:</span></span>

<span data-ttu-id="966e6-124">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="966e6-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="966e6-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="966e6-125">-DefaultProfile</span></span>
<span data-ttu-id="966e6-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="966e6-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="966e6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="966e6-127">CommonParameters</span></span>
<span data-ttu-id="966e6-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="966e6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="966e6-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="966e6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="966e6-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="966e6-130">INPUTS</span></span>

## <span data-ttu-id="966e6-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="966e6-131">OUTPUTS</span></span>

### <span data-ttu-id="966e6-132">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="966e6-132">BatchAccountContext</span></span>

## <span data-ttu-id="966e6-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="966e6-133">NOTES</span></span>

## <span data-ttu-id="966e6-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="966e6-134">RELATED LINKS</span></span>

[<span data-ttu-id="966e6-135">Get-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="966e6-135">Get-AzureRmBatchAccount</span></span>](./Get-AzureRmBatchAccount.md)

[<span data-ttu-id="966e6-136">Remove-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="966e6-136">Remove-AzureRmBatchAccount</span></span>](./Remove-AzureRmBatchAccount.md)

[<span data-ttu-id="966e6-137">Satz-AzureRmBatchAccount</span><span class="sxs-lookup"><span data-stu-id="966e6-137">Set-AzureRmBatchAccount</span></span>](./Set-AzureRmBatchAccount.md)

[<span data-ttu-id="966e6-138">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="966e6-138">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)
