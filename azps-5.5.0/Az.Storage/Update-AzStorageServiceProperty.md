---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageServiceProperty.md
ms.openlocfilehash: e94bb90ffeda257dd024c1cf9b834764455cd6aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164689"
---
# <span data-ttu-id="cd8c4-101">Update-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="cd8c4-101">Update-AzStorageServiceProperty</span></span>

## <span data-ttu-id="cd8c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd8c4-102">SYNOPSIS</span></span>
<span data-ttu-id="cd8c4-103">Ändert die Eigenschaften für den Azure Storage-Dienst.</span><span class="sxs-lookup"><span data-stu-id="cd8c4-103">Modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="cd8c4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cd8c4-104">SYNTAX</span></span>

```
Update-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cd8c4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cd8c4-105">DESCRIPTION</span></span>
<span data-ttu-id="cd8c4-106">Das **Cmdlet "Update-AzStorageServiceProperty"** ändert die Eigenschaften für den Azure Storage-Dienst.</span><span class="sxs-lookup"><span data-stu-id="cd8c4-106">The **Update-AzStorageServiceProperty** cmdlet modifies the properties for the Azure Storage service.</span></span>

## <span data-ttu-id="cd8c4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cd8c4-107">EXAMPLES</span></span>

### <span data-ttu-id="cd8c4-108">Beispiel 1: Festlegen von Blob Service DefaultServiceVersion auf 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="cd8c4-108">Example 1: Set Blob Service DefaultServiceVersion to 2017-04-17</span></span>
```
C:\PS>Update-AzStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

<span data-ttu-id="cd8c4-109">Dieser Befehl Set the DefaultServiceVersion of Blob Service to 2017-04-17</span><span class="sxs-lookup"><span data-stu-id="cd8c4-109">This command Set the DefaultServiceVersion of Blob Service to 2017-04-17</span></span>

## <span data-ttu-id="cd8c4-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd8c4-110">PARAMETERS</span></span>

### <span data-ttu-id="cd8c4-111">-Context</span><span class="sxs-lookup"><span data-stu-id="cd8c4-111">-Context</span></span>
<span data-ttu-id="cd8c4-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="cd8c4-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="cd8c4-113">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd8c4-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd8c4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd8c4-114">-DefaultProfile</span></span>
<span data-ttu-id="cd8c4-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd8c4-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd8c4-116">-DefaultServiceVersion</span><span class="sxs-lookup"><span data-stu-id="cd8c4-116">-DefaultServiceVersion</span></span>
<span data-ttu-id="cd8c4-117">"DefaultServiceVersion" gibt die Standardversion an, die für Anforderungen an den Blob Service verwendet werden soll, wenn die Version einer eingehenden Anforderung nicht angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="cd8c4-117">DefaultServiceVersion indicates the default version to use for requests to the Blob service if an incoming request's version is not specified.</span></span> <span data-ttu-id="cd8c4-118">Mögliche Werte sind Version 2008-10-27 und alle neueren Versionen.</span><span class="sxs-lookup"><span data-stu-id="cd8c4-118">Possible values include version 2008-10-27 and all more recent versions.</span></span> <span data-ttu-id="cd8c4-119">Weitere Details finden Sie unter https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span><span class="sxs-lookup"><span data-stu-id="cd8c4-119">See more details in https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-az-storage-services</span></span>

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

### <span data-ttu-id="cd8c4-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd8c4-120">-PassThru</span></span>
<span data-ttu-id="cd8c4-121">Anzeigen von ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="cd8c4-121">Display ServiceProperties</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd8c4-122">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="cd8c4-122">-ServiceType</span></span>
<span data-ttu-id="cd8c4-123">Gibt den Speicherdiensttyp an.</span><span class="sxs-lookup"><span data-stu-id="cd8c4-123">Specifies the storage service type.</span></span>
<span data-ttu-id="cd8c4-124">Dieses Cmdlet ruft die Protokolleigenschaften für den Diensttyp ab, den dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="cd8c4-124">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="cd8c4-125">Die zulässigen Werte für diesen Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="cd8c4-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cd8c4-126">BLOB</span><span class="sxs-lookup"><span data-stu-id="cd8c4-126">Blob</span></span> 
- <span data-ttu-id="cd8c4-127">Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd8c4-127">Table</span></span>
- <span data-ttu-id="cd8c4-128">Warteschlange</span><span class="sxs-lookup"><span data-stu-id="cd8c4-128">Queue</span></span>
- <span data-ttu-id="cd8c4-129">Datei</span><span class="sxs-lookup"><span data-stu-id="cd8c4-129">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd8c4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cd8c4-130">-Confirm</span></span>
<span data-ttu-id="cd8c4-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cd8c4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd8c4-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cd8c4-132">-WhatIf</span></span>
<span data-ttu-id="cd8c4-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cd8c4-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cd8c4-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cd8c4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd8c4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd8c4-135">CommonParameters</span></span>
<span data-ttu-id="cd8c4-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd8c4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd8c4-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd8c4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd8c4-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cd8c4-138">INPUTS</span></span>

### <span data-ttu-id="cd8c4-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cd8c4-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cd8c4-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cd8c4-140">OUTPUTS</span></span>

### <span data-ttu-id="cd8c4-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="cd8c4-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="cd8c4-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cd8c4-142">NOTES</span></span>

## <span data-ttu-id="cd8c4-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cd8c4-143">RELATED LINKS</span></span>
