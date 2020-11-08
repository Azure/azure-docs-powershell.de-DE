---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
ms.openlocfilehash: c0b283c7645426af9397fd675fde825ff0b5f087
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166787"
---
# <span data-ttu-id="45578-101">Get-AzStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="45578-101">Get-AzStorageAccountNameAvailability</span></span>

## <span data-ttu-id="45578-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="45578-102">SYNOPSIS</span></span>
<span data-ttu-id="45578-103">Überprüft die Verfügbarkeit eines Speicherkonto namens.</span><span class="sxs-lookup"><span data-stu-id="45578-103">Checks the availability of a Storage account name.</span></span>

## <span data-ttu-id="45578-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="45578-104">SYNTAX</span></span>

```
Get-AzStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45578-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45578-105">DESCRIPTION</span></span>
<span data-ttu-id="45578-106">Das Cmdlet " **Get-AzStorageAccountNameAvailability** " überprüft, ob der Name eines Azure-speicherkontos gültig und für die Verwendung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="45578-106">The **Get-AzStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="45578-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45578-107">EXAMPLES</span></span>

### <span data-ttu-id="45578-108">Beispiel 1: Überprüfen der Verfügbarkeit eines Speicherkonto namens</span><span class="sxs-lookup"><span data-stu-id="45578-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="45578-109">Dieser Befehl überprüft die Verfügbarkeit des Namens ContosoStorage03.</span><span class="sxs-lookup"><span data-stu-id="45578-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="45578-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="45578-110">PARAMETERS</span></span>

### <span data-ttu-id="45578-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45578-111">-DefaultProfile</span></span>
<span data-ttu-id="45578-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="45578-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45578-113">-Name</span><span class="sxs-lookup"><span data-stu-id="45578-113">-Name</span></span>
<span data-ttu-id="45578-114">Gibt den Namen des speicherkontos an, das von diesem Cmdlet überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="45578-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="45578-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45578-115">CommonParameters</span></span>
<span data-ttu-id="45578-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45578-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45578-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45578-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45578-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="45578-118">INPUTS</span></span>

### <span data-ttu-id="45578-119">System. String</span><span class="sxs-lookup"><span data-stu-id="45578-119">System.String</span></span>

## <span data-ttu-id="45578-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="45578-120">OUTPUTS</span></span>

### <span data-ttu-id="45578-121">Microsoft. Azure. Management. Storage. Models. CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="45578-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="45578-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="45578-122">NOTES</span></span>

## <span data-ttu-id="45578-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="45578-123">RELATED LINKS</span></span>

[<span data-ttu-id="45578-124">Azure Storage Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="45578-124">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


