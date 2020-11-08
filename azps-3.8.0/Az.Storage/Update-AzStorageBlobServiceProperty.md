---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageblobserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageBlobServiceProperty.md
ms.openlocfilehash: b7d6299af3f56dd8f09c73171ab6630cbbb9bc96
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93997226"
---
# <span data-ttu-id="8ebaa-101">Update-AzStorageBlobServiceProperty</span><span class="sxs-lookup"><span data-stu-id="8ebaa-101">Update-AzStorageBlobServiceProperty</span></span>

## <span data-ttu-id="8ebaa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ebaa-102">SYNOPSIS</span></span>
<span data-ttu-id="8ebaa-103">Ändert die Diensteigenschaften für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="8ebaa-103">Modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="8ebaa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ebaa-104">SYNTAX</span></span>

### <span data-ttu-id="8ebaa-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="8ebaa-105">AccountName (Default)</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultServiceVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8ebaa-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="8ebaa-106">AccountObject</span></span>
```
Update-AzStorageBlobServiceProperty -StorageAccount <PSStorageAccount> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8ebaa-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="8ebaa-107">BlobServicePropertiesResourceId</span></span>
```
Update-AzStorageBlobServiceProperty [-ResourceId] <String> [-DefaultServiceVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ebaa-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ebaa-108">DESCRIPTION</span></span>
<span data-ttu-id="8ebaa-109">Das Cmdlet **Update-AzStorageBlobServiceProperty** ändert die Diensteigenschaften für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="8ebaa-109">The **Update-AzStorageBlobServiceProperty** cmdlet modifies the service properties for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="8ebaa-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ebaa-110">EXAMPLES</span></span>

### <span data-ttu-id="8ebaa-111">Beispiel 1: Einrichten des BLOB-Diensts DefaultServiceVersion auf 2018-03-28</span><span class="sxs-lookup"><span data-stu-id="8ebaa-111">Example 1: Set Blob service DefaultServiceVersion to 2018-03-28</span></span>
```
C:\PS> Update-AzStorageBlobServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -DefaultServiceVersion 2018-03-28 

StorageAccountName ResourceGroupName DefaultServiceVersion DeleteRetentionPolicy.Enabled DeleteRetentionPolicy.Days
------------------ ----------------- --------------------- ----------------------------- --------------------------
myresourcegroup    mystorageaccount  2018-03-28            False                                                   
```

<span data-ttu-id="8ebaa-112">Dieser Befehl legt die DefaultServiceVersion des BLOB-Diensts auf 2018-03-28 fest.</span><span class="sxs-lookup"><span data-stu-id="8ebaa-112">This command sets the DefaultServiceVersion of Blob Service to 2018-03-28.</span></span>

## <span data-ttu-id="8ebaa-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ebaa-113">PARAMETERS</span></span>

### <span data-ttu-id="8ebaa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ebaa-114">-DefaultProfile</span></span>
<span data-ttu-id="8ebaa-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8ebaa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ebaa-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="8ebaa-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="8ebaa-117">Standardmäßige Dienst Version zum Festlegen</span><span class="sxs-lookup"><span data-stu-id="8ebaa-117">Default Service Version to Set</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebaa-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ebaa-118">-ResourceGroupName</span></span>
<span data-ttu-id="8ebaa-119">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8ebaa-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="8ebaa-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8ebaa-120">-ResourceId</span></span>
<span data-ttu-id="8ebaa-121">Geben Sie eine Ressourcen-ID des speicherkontos oder eine Ressourcen-ID für BLOB-Diensteigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="8ebaa-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="8ebaa-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ebaa-122">-StorageAccount</span></span>
<span data-ttu-id="8ebaa-123">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="8ebaa-123">Storage account object</span></span>

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

### <span data-ttu-id="8ebaa-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="8ebaa-124">-StorageAccountName</span></span>
<span data-ttu-id="8ebaa-125">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="8ebaa-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="8ebaa-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8ebaa-126">-Confirm</span></span>
<span data-ttu-id="8ebaa-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8ebaa-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebaa-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ebaa-128">-WhatIf</span></span>
<span data-ttu-id="8ebaa-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8ebaa-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8ebaa-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ebaa-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ebaa-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ebaa-131">CommonParameters</span></span>
<span data-ttu-id="8ebaa-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ebaa-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ebaa-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ebaa-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ebaa-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ebaa-134">INPUTS</span></span>

### <span data-ttu-id="8ebaa-135">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="8ebaa-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="8ebaa-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8ebaa-136">System.String</span></span>

## <span data-ttu-id="8ebaa-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ebaa-137">OUTPUTS</span></span>

### <span data-ttu-id="8ebaa-138">Microsoft. Azure. Commands. Management. Storage. Models. PSBlobServiceProperties</span><span class="sxs-lookup"><span data-stu-id="8ebaa-138">Microsoft.Azure.Commands.Management.Storage.Models.PSBlobServiceProperties</span></span>

## <span data-ttu-id="8ebaa-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ebaa-139">NOTES</span></span>

## <span data-ttu-id="8ebaa-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ebaa-140">RELATED LINKS</span></span>
