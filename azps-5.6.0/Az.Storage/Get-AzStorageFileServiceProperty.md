---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
ms.openlocfilehash: 9503f62667405c8e7a652bffc150a747eadb40f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101933360"
---
# <span data-ttu-id="8a06b-101">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8a06b-101">Get-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="8a06b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a06b-102">SYNOPSIS</span></span>
<span data-ttu-id="8a06b-103">Ruft Diensteigenschaften für Azure Storage File-Dienste ab.</span><span class="sxs-lookup"><span data-stu-id="8a06b-103">Gets service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="8a06b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8a06b-104">SYNTAX</span></span>

### <span data-ttu-id="8a06b-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8a06b-105">AccountName (Default)</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8a06b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="8a06b-106">AccountObject</span></span>
```
Get-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a06b-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="8a06b-107">FileServicePropertiesResourceId</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a06b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8a06b-108">DESCRIPTION</span></span>
<span data-ttu-id="8a06b-109">Das **Get-AzStorageFileServiceProperty-Cmdlet** ruft die Diensteigenschaften für Azure Storage File Services ab.</span><span class="sxs-lookup"><span data-stu-id="8a06b-109">The **Get-AzStorageFileServiceProperty** cmdlet gets the service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="8a06b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8a06b-110">EXAMPLES</span></span>

### <span data-ttu-id="8a06b-111">Beispiel 1: Azure Storage File Services-Eigenschaft eines angegebenen Speicherkontos herunterladen</span><span class="sxs-lookup"><span data-stu-id="8a06b-111">Example 1: Get  Azure Storage File services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName                            : mystorageaccount
ResourceGroupName                             : myresourcegroup
ShareDeleteRetentionPolicy.Enabled            : True
ShareDeleteRetentionPolicy.Days               : 3
```

<span data-ttu-id="8a06b-112">Dieser Befehl ruft die Dateidiensteigenschaft eines angegebenen Speicherkontos ab.</span><span class="sxs-lookup"><span data-stu-id="8a06b-112">This command gets the File services property of a specified Storage Account.</span></span>

## <span data-ttu-id="8a06b-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8a06b-113">PARAMETERS</span></span>

### <span data-ttu-id="8a06b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a06b-114">-DefaultProfile</span></span>
<span data-ttu-id="8a06b-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8a06b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a06b-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a06b-116">-ResourceGroupName</span></span>
<span data-ttu-id="8a06b-117">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="8a06b-117">Resource Group Name.</span></span>

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

### <span data-ttu-id="8a06b-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a06b-118">-ResourceId</span></span>
<span data-ttu-id="8a06b-119">Geben Sie eine Ressourcen-ID des Speicherkontos oder eine Dateidiensteigenschaften-Ressourcen-ID ein.</span><span class="sxs-lookup"><span data-stu-id="8a06b-119">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: FileServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a06b-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8a06b-120">-StorageAccount</span></span>
<span data-ttu-id="8a06b-121">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="8a06b-121">Storage account object</span></span>

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

### <span data-ttu-id="8a06b-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8a06b-122">-StorageAccountName</span></span>
<span data-ttu-id="8a06b-123">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="8a06b-123">Storage Account Name.</span></span>

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

### <span data-ttu-id="8a06b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a06b-124">CommonParameters</span></span>
<span data-ttu-id="8a06b-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a06b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a06b-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a06b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a06b-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8a06b-127">INPUTS</span></span>

### <span data-ttu-id="8a06b-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8a06b-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="8a06b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="8a06b-129">System.String</span></span>

## <span data-ttu-id="8a06b-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8a06b-130">OUTPUTS</span></span>

### <span data-ttu-id="8a06b-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="8a06b-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="8a06b-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8a06b-132">NOTES</span></span>

## <span data-ttu-id="8a06b-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8a06b-133">RELATED LINKS</span></span>
