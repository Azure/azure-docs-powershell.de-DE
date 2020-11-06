---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
ms.openlocfilehash: 08d997caef7280d922a01dbea127bd4db64cd28f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93475926"
---
# <span data-ttu-id="36f59-101">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="36f59-101">Get-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="36f59-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36f59-102">SYNOPSIS</span></span>
<span data-ttu-id="36f59-103">Ruft die Zugriffstasten für ein Azure Storage-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="36f59-103">Gets the access keys for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36f59-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36f59-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36f59-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36f59-105">DESCRIPTION</span></span>
<span data-ttu-id="36f59-106">Das Cmdlet " **Get-AzureRmStorageAccountKey** " Ruft die Zugriffstasten für ein Azure Storage-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="36f59-106">The **Get-AzureRmStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="36f59-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36f59-107">EXAMPLES</span></span>

### <span data-ttu-id="36f59-108">Beispiel 1: Abrufen der Zugriffstasten für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="36f59-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="36f59-109">Dieser Befehl ruft die Schlüssel für das angegebene Azure-Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="36f59-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="36f59-110">Beispiel 2: Abrufen einer bestimmten Zugriffstaste für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="36f59-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

## <span data-ttu-id="36f59-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="36f59-111">PARAMETERS</span></span>

### <span data-ttu-id="36f59-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36f59-112">-DefaultProfile</span></span>
<span data-ttu-id="36f59-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="36f59-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36f59-114">-Name</span><span class="sxs-lookup"><span data-stu-id="36f59-114">-Name</span></span>
<span data-ttu-id="36f59-115">Gibt den Namen des speicherkontos an, für das dieses Cmdlet Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="36f59-115">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="36f59-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36f59-116">-ResourceGroupName</span></span>
<span data-ttu-id="36f59-117">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="36f59-117">Specifies the name of the resource group that contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36f59-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36f59-118">CommonParameters</span></span>
<span data-ttu-id="36f59-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36f59-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36f59-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36f59-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36f59-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36f59-121">INPUTS</span></span>

### <span data-ttu-id="36f59-122">System. String</span><span class="sxs-lookup"><span data-stu-id="36f59-122">System.String</span></span>

## <span data-ttu-id="36f59-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36f59-123">OUTPUTS</span></span>

### <span data-ttu-id="36f59-124">Microsoft. Azure. Management. Storage. Models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="36f59-124">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="36f59-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="36f59-125">NOTES</span></span>

## <span data-ttu-id="36f59-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36f59-126">RELATED LINKS</span></span>

[<span data-ttu-id="36f59-127">Neu – AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="36f59-127">New-AzureRmStorageAccountKey</span></span>](./New-AzureRmStorageAccountKey.md)


