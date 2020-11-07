---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 8590c9566cf84648dc8668d3fb49ac19b8d4787d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662343"
---
# <span data-ttu-id="982ca-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="982ca-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="982ca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="982ca-102">SYNOPSIS</span></span>
<span data-ttu-id="982ca-103">Überprüft die Verfügbarkeit eines Speicherkonto namens.</span><span class="sxs-lookup"><span data-stu-id="982ca-103">Checks the availability of a storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="982ca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="982ca-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="982ca-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="982ca-105">DESCRIPTION</span></span>
<span data-ttu-id="982ca-106">Das Cmdlet " **Get-AzureRmStorageAccountNameAvailability** " überprüft, ob der Name eines Azure-speicherkontos gültig und für die Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="982ca-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="982ca-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="982ca-107">EXAMPLES</span></span>

### <span data-ttu-id="982ca-108">Beispiel 1: Überprüfen der Verfügbarkeit eines Speicherkonto namens</span><span class="sxs-lookup"><span data-stu-id="982ca-108">Example 1: Check availability of a storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'ContosoStorage03'
```

<span data-ttu-id="982ca-109">Dieser Befehl überprüft die Verfügbarkeit des Namens ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="982ca-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="982ca-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="982ca-110">PARAMETERS</span></span>

### <span data-ttu-id="982ca-111">-Name</span><span class="sxs-lookup"><span data-stu-id="982ca-111">-Name</span></span>
<span data-ttu-id="982ca-112">Gibt den Namen des speicherkontos an, das von diesem Cmdlet überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="982ca-112">Specifies the name of the Storage account that this cmdlet checks.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="982ca-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="982ca-113">CommonParameters</span></span>
<span data-ttu-id="982ca-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="982ca-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="982ca-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="982ca-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="982ca-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="982ca-116">INPUTS</span></span>

### <span data-ttu-id="982ca-117">Keine</span><span class="sxs-lookup"><span data-stu-id="982ca-117">None</span></span>
<span data-ttu-id="982ca-118">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="982ca-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="982ca-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="982ca-119">OUTPUTS</span></span>

## <span data-ttu-id="982ca-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="982ca-120">NOTES</span></span>

## <span data-ttu-id="982ca-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="982ca-121">RELATED LINKS</span></span>

[<span data-ttu-id="982ca-122">Azure Storage Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="982ca-122">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)
