---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: F6EA099A-D588-49AE-9D2C-865BC32685BA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountnameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountNameAvailability.md
ms.openlocfilehash: c0b283c7645426af9397fd675fde825ff0b5f087
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376254"
---
# <span data-ttu-id="07bf8-101">Get-AzStorageAccountNameAvailability</span><span class="sxs-lookup"><span data-stu-id="07bf8-101">Get-AzStorageAccountNameAvailability</span></span>

## <span data-ttu-id="07bf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07bf8-102">SYNOPSIS</span></span>
<span data-ttu-id="07bf8-103">Überprüft die Verfügbarkeit eines Speicherkontonamens.</span><span class="sxs-lookup"><span data-stu-id="07bf8-103">Checks the availability of a Storage account name.</span></span>

## <span data-ttu-id="07bf8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07bf8-104">SYNTAX</span></span>

```
Get-AzStorageAccountNameAvailability [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07bf8-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07bf8-105">DESCRIPTION</span></span>
<span data-ttu-id="07bf8-106">Das **Cmdlet "Get-AzStorageAccountNameAvailability"** überprüft, ob der Name eines Azure Storage-Kontos gültig und verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="07bf8-106">The **Get-AzStorageAccountNameAvailability** cmdlet checks whether the name of an Azure Storage account is valid and available to use.</span></span>

## <span data-ttu-id="07bf8-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="07bf8-107">EXAMPLES</span></span>

### <span data-ttu-id="07bf8-108">Beispiel 1: Überprüfen der Verfügbarkeit eines Speicherkontonamens</span><span class="sxs-lookup"><span data-stu-id="07bf8-108">Example 1: Check availability of a Storage account name</span></span>
```
PS C:\>Get-AzStorageAccountNameAvailability -Name 'contosostorage03'
```

<span data-ttu-id="07bf8-109">Mit diesem Befehl wird die Verfügbarkeit des Namens "ContosoStorage03" überprüft.</span><span class="sxs-lookup"><span data-stu-id="07bf8-109">This command checks the availability of the name ContosoStorage03.</span></span>

## <span data-ttu-id="07bf8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07bf8-110">PARAMETERS</span></span>

### <span data-ttu-id="07bf8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07bf8-111">-DefaultProfile</span></span>
<span data-ttu-id="07bf8-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="07bf8-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07bf8-113">-Name</span><span class="sxs-lookup"><span data-stu-id="07bf8-113">-Name</span></span>
<span data-ttu-id="07bf8-114">Gibt den Namen des Speicherkontos an, das von diesem Cmdlet überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="07bf8-114">Specifies the name of the Storage account that this cmdlet checks.</span></span>

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

### <span data-ttu-id="07bf8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07bf8-115">CommonParameters</span></span>
<span data-ttu-id="07bf8-116">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07bf8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07bf8-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07bf8-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07bf8-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="07bf8-118">INPUTS</span></span>

### <span data-ttu-id="07bf8-119">System.String</span><span class="sxs-lookup"><span data-stu-id="07bf8-119">System.String</span></span>

## <span data-ttu-id="07bf8-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="07bf8-120">OUTPUTS</span></span>

### <span data-ttu-id="07bf8-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span><span class="sxs-lookup"><span data-stu-id="07bf8-121">Microsoft.Azure.Management.Storage.Models.CheckNameAvailabilityResult</span></span>

## <span data-ttu-id="07bf8-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="07bf8-122">NOTES</span></span>

## <span data-ttu-id="07bf8-123">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="07bf8-123">RELATED LINKS</span></span>

[<span data-ttu-id="07bf8-124">Azure Storage Manager-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="07bf8-124">Azure Storage Manager Cmdlets</span></span>](./Az.Storage.md)


