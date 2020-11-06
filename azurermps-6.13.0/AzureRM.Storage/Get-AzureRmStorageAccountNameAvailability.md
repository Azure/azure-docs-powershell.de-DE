---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountNameAvailability.md
ms.openlocfilehash: 402e3fdfe108486cd356af8a20ea06793f533937
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502821"
---
# <span data-ttu-id="61980-101">Get-AzureRmStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="61980-101">Get-AzureRmStorageAccountNameAvailability</span></span>

## <span data-ttu-id="61980-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="61980-102">SYNOPSIS</span></span>
<span data-ttu-id="61980-103">Überprüft die Verfügbarkeit eines Speicherkonto namens.</span><span class="sxs-lookup"><span data-stu-id="61980-103">Checks the availability of a Storage account name.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="61980-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="61980-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61980-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="61980-105">DESCRIPTION</span></span>
<span data-ttu-id="61980-106">Das Cmdlet " **Get-AzureRmStorageAccountNameAvailability** " überprüft, ob der Name eines Azure-speicherkontos gültig und für die Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="61980-106">The **Get-AzureRmStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="61980-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="61980-107">EXAMPLES</span></span>

### <span data-ttu-id="61980-108">Beispiel 1: Überprüfen der Verfügbarkeit eines Speicherkonto namens</span><span class="sxs-lookup"><span data-stu-id="61980-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzureRmStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="61980-109">Dieser Befehl überprüft die Verfügbarkeit des Namens ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="61980-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="61980-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="61980-110">PARAMETERS</span></span>

### <span data-ttu-id="61980-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61980-111">-DefaultProfile</span></span>
<span data-ttu-id="61980-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="61980-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61980-113">-Name</span><span class="sxs-lookup"><span data-stu-id="61980-113">-Name</span></span>
<span data-ttu-id="61980-114">Gibt den Namen des speicherkontos an, das von diesem Cmdlet überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="61980-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61980-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61980-115">CommonParameters</span></span>
<span data-ttu-id="61980-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61980-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61980-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61980-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61980-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="61980-118">INPUTS</span></span>

### <span data-ttu-id="61980-119">System. String</span><span class="sxs-lookup"><span data-stu-id="61980-119">System.String</span></span>

## <span data-ttu-id="61980-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="61980-120">OUTPUTS</span></span>

### <span data-ttu-id="61980-121">Microsoft. Azure. Management. Storage. Models. CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="61980-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="61980-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="61980-122">NOTES</span></span>

## <span data-ttu-id="61980-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="61980-123">RELATED LINKS</span></span>

[<span data-ttu-id="61980-124">Azure Storage Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="61980-124">Azure Storage Manager Cmdlets</span></span>](./AzureRM.Storage.md)


