---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
ms.openlocfilehash: 23066206607289d531f2e2eaa14f90660360a705
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478173"
---
# <span data-ttu-id="efc7b-101">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="efc7b-101">Get-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="efc7b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="efc7b-102">SYNOPSIS</span></span>
<span data-ttu-id="efc7b-103">Ruft die Zugriffstasten für ein Azure Storage-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="efc7b-103">Gets the access keys for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="efc7b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="efc7b-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [<CommonParameters>]
```

## <span data-ttu-id="efc7b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="efc7b-105">DESCRIPTION</span></span>
<span data-ttu-id="efc7b-106">Das Cmdlet " **Get-AzureRmStorageAccountKey** " Ruft die Zugriffstasten für ein Azure Storage-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="efc7b-106">The **Get-AzureRmStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="efc7b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="efc7b-107">EXAMPLES</span></span>

### <span data-ttu-id="efc7b-108">Beispiel 1: Abrufen der Zugriffstasten für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="efc7b-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="efc7b-109">Dieser Befehl ruft die Schlüssel für das angegebene Azure-Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="efc7b-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="efc7b-110">Beispiel 2: Abrufen einer bestimmten Zugriffstaste für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="efc7b-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Key1
```

## <span data-ttu-id="efc7b-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="efc7b-111">PARAMETERS</span></span>

### <span data-ttu-id="efc7b-112">-Name</span><span class="sxs-lookup"><span data-stu-id="efc7b-112">-Name</span></span>
<span data-ttu-id="efc7b-113">Gibt den Namen des speicherkontos an, für das dieses Cmdlet Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="efc7b-113">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="efc7b-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="efc7b-114">-ResourceGroupName</span></span>
<span data-ttu-id="efc7b-115">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="efc7b-115">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="efc7b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efc7b-116">CommonParameters</span></span>
<span data-ttu-id="efc7b-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="efc7b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efc7b-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="efc7b-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efc7b-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="efc7b-119">INPUTS</span></span>

### <span data-ttu-id="efc7b-120">Keine</span><span class="sxs-lookup"><span data-stu-id="efc7b-120">None</span></span>
<span data-ttu-id="efc7b-121">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="efc7b-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="efc7b-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="efc7b-122">OUTPUTS</span></span>

## <span data-ttu-id="efc7b-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="efc7b-123">NOTES</span></span>

## <span data-ttu-id="efc7b-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="efc7b-124">RELATED LINKS</span></span>

[<span data-ttu-id="efc7b-125">Neu – AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="efc7b-125">New-AzureRmStorageAccountKey</span></span>](./New-AzureRmStorageAccountKey.md)
