---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobServiceProperty.md
ms.openlocfilehash: 03e77346c14e095a11720b8cdaf930eaaa397f8a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658877"
---
# <span data-ttu-id="57c7b-101">Get-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="57c7b-101">Get-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="57c7b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="57c7b-102">SYNOPSIS</span></span>
<span data-ttu-id="57c7b-103">Ruft Diensteigenschaften für Azure Storage-BLOB-Dienste ab.</span><span class="sxs-lookup"><span data-stu-id="57c7b-103">Gets service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="57c7b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="57c7b-104">SYNTAX</span></span>

### <span data-ttu-id="57c7b-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="57c7b-105">AccountName (Default)</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="57c7b-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="57c7b-106">AccountObject</span></span>
```
Get-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="57c7b-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="57c7b-107">BlobServicePropertiesResourceId</span></span>
```
Get-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="57c7b-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57c7b-108">DESCRIPTION</span></span>
<span data-ttu-id="57c7b-109">Das Cmdlet " **Get-AzStorageBlobServiceProperty** " Ruft die Diensteigenschaften für Azure Storage-BLOB-Dienste ab.</span><span class="sxs-lookup"><span data-stu-id="57c7b-109">The **Get-AzStorageBlobServiceProperty** cmdlet gets the service properties for Azure Storage Blob services.</span></span>

## <span data-ttu-id="57c7b-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="57c7b-110">EXAMPLES</span></span>

### <span data-ttu-id="57c7b-111">Beispiel 1: Abrufen der Azure Storage BLOB Services-Eigenschaft eines angegebenen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="57c7b-111">Example 1: Get  Azure Storage Blob services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days
------------------ ----------------- --------------------- ----------------------------- --------------------------
myresourcegroup    mystorageaccount  2018-03-28            False
```

<span data-ttu-id="57c7b-112">Mit diesem Befehl wird die BLOB Services-Eigenschaft eines angegebenen speicherkontos abgerufen.</span><span class="sxs-lookup"><span data-stu-id="57c7b-112">This command gets the Blob services property of a specified Storage Account.</span></span>

## <span data-ttu-id="57c7b-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="57c7b-113">PARAMETERS</span></span>

### <span data-ttu-id="57c7b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57c7b-114">-DefaultProfile</span></span>
<span data-ttu-id="57c7b-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="57c7b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57c7b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="57c7b-116">-ResourceGroupName</span></span>
<span data-ttu-id="57c7b-117">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="57c7b-117">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c7b-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="57c7b-118">-ResourceId</span></span>
<span data-ttu-id="57c7b-119">Ressourcen-ID für BLOB-Diensteigenschaften.</span><span class="sxs-lookup"><span data-stu-id="57c7b-119">Blob Service Properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57c7b-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="57c7b-120">-StorageAccount</span></span>
<span data-ttu-id="57c7b-121">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="57c7b-121">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57c7b-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="57c7b-122">-StorageAccountName</span></span>
<span data-ttu-id="57c7b-123">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="57c7b-123">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57c7b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57c7b-124">CommonParameters</span></span>
<span data-ttu-id="57c7b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57c7b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57c7b-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57c7b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57c7b-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="57c7b-127">INPUTS</span></span>

### <span data-ttu-id="57c7b-128">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="57c7b-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="57c7b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="57c7b-129">System.String</span></span>

## <span data-ttu-id="57c7b-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="57c7b-130">OUTPUTS</span></span>

### <span data-ttu-id="57c7b-131">Microsoft. Azure. Commands. Management. Storage. Models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="57c7b-131">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="57c7b-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="57c7b-132">NOTES</span></span>

## <span data-ttu-id="57c7b-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="57c7b-133">RELATED LINKS</span></span>
