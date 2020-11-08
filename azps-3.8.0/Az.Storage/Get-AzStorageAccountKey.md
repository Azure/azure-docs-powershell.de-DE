---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: faecfdf62892faba2f7ec1241d7e02daa1e6ed12
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997002"
---
# <span data-ttu-id="bd2f6-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="bd2f6-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="bd2f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bd2f6-102">SYNOPSIS</span></span>
<span data-ttu-id="bd2f6-103">Ruft die Zugriffstasten für ein Azure Storage-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="bd2f6-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="bd2f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd2f6-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd2f6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bd2f6-105">DESCRIPTION</span></span>
<span data-ttu-id="bd2f6-106">Das Cmdlet " **Get-AzStorageAccountKey** " Ruft die Zugriffstasten für ein Azure Storage-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="bd2f6-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="bd2f6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bd2f6-107">EXAMPLES</span></span>

### <span data-ttu-id="bd2f6-108">Beispiel 1: Abrufen der Zugriffstasten für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="bd2f6-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="bd2f6-109">Dieser Befehl ruft die Schlüssel für das angegebene Azure-Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="bd2f6-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="bd2f6-110">Beispiel 2: Abrufen einer bestimmten Zugriffstaste für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="bd2f6-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

## <span data-ttu-id="bd2f6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd2f6-111">PARAMETERS</span></span>

### <span data-ttu-id="bd2f6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd2f6-112">-DefaultProfile</span></span>
<span data-ttu-id="bd2f6-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bd2f6-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bd2f6-114">-Name</span><span class="sxs-lookup"><span data-stu-id="bd2f6-114">-Name</span></span>
<span data-ttu-id="bd2f6-115">Gibt den Namen des speicherkontos an, für das dieses Cmdlet Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="bd2f6-115">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="bd2f6-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd2f6-116">-ResourceGroupName</span></span>
<span data-ttu-id="bd2f6-117">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="bd2f6-117">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="bd2f6-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd2f6-118">CommonParameters</span></span>
<span data-ttu-id="bd2f6-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd2f6-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd2f6-120">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd2f6-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd2f6-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bd2f6-121">INPUTS</span></span>

### <span data-ttu-id="bd2f6-122">System. String</span><span class="sxs-lookup"><span data-stu-id="bd2f6-122">System.String</span></span>

## <span data-ttu-id="bd2f6-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bd2f6-123">OUTPUTS</span></span>

### <span data-ttu-id="bd2f6-124">Microsoft. Azure. Management. Storage. Models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="bd2f6-124">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="bd2f6-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="bd2f6-125">NOTES</span></span>

## <span data-ttu-id="bd2f6-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bd2f6-126">RELATED LINKS</span></span>

[<span data-ttu-id="bd2f6-127">Neu – AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="bd2f6-127">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


