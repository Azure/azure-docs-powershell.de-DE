---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/new-azwebappazurestoragepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
ms.openlocfilehash: b30a7736c1d3971bcdd4d7b3b776b0c439e9395b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928792"
---
# <span data-ttu-id="fc855-101">New-AzWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="fc855-101">New-AzWebAppAzureStoragePath</span></span>

## <span data-ttu-id="fc855-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc855-102">SYNOPSIS</span></span>
<span data-ttu-id="fc855-103">Erstellt ein -Objekt, das einen Azure Storage-Pfad darstellt, der in einer Web App bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc855-103">Creates an object that represents an Azure Storage path to be mounted in a Web App.</span></span> <span data-ttu-id="fc855-104">Er soll als Parameter (-AzureStoragePath) verwendet werden, Set-AzWebApp und Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="fc855-104">It is meant to be used as a parameter (-AzureStoragePath) to Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <span data-ttu-id="fc855-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc855-105">SYNTAX</span></span>

```
New-AzWebAppAzureStoragePath -Name <String> -Type <AzureStorageType> -AccountName <String> -ShareName <String>
 -AccessKey <String> -MountPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc855-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fc855-106">DESCRIPTION</span></span>
<span data-ttu-id="fc855-107">Erstellt ein -Objekt, das einen Azure Storage-Pfad repräsentiert, der in einer Web App bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="fc855-107">Creates an object that represent an Azure Storage path to be mounted inside a Web App.</span></span>

## <span data-ttu-id="fc855-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fc855-108">EXAMPLES</span></span>

### <span data-ttu-id="fc855-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fc855-109">Example 1</span></span>
```powershell
PS C:\> $storagePath1 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount1" -AccountName "myaccount.files.core.windows.net" -Type AzureFiles -ShareName "someShareName" -AccessKey "some access key"
-MountPath "C:\myFolderInsideTheContainerWebApp" 

PS C:\> $storagePath2 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount2" -AccountName "myaccount2.files.core.windows.net" -Type AzureFiles -ShareName "someShareName2" -AccessKey "some access key 2"
-MountPath "C:\myFolderInsideTheContainerWebApp2" 

PS C:\> Set-AzWebApp -ResourceGroup myresourcegroup -Name myapp -AzureStoragePath $storagepath1, $storagePath2
```

## <span data-ttu-id="fc855-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="fc855-110">PARAMETERS</span></span>

### <span data-ttu-id="fc855-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="fc855-111">-AccessKey</span></span>
<span data-ttu-id="fc855-112">Zugriffsschlüssel für das Azure Storage-Konto</span><span class="sxs-lookup"><span data-stu-id="fc855-112">Access key to the Azure Storage account</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc855-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="fc855-113">-AccountName</span></span>
<span data-ttu-id="fc855-114">Azure Storage-Kontoname.</span><span class="sxs-lookup"><span data-stu-id="fc855-114">Azure Storage account name.</span></span>
<span data-ttu-id="fc855-115">Beispiel: myfilestorageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="fc855-115">E.g.: myfilestorageaccount.file.core.windows.net</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc855-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc855-116">-DefaultProfile</span></span>
<span data-ttu-id="fc855-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fc855-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc855-118">-MountPath</span><span class="sxs-lookup"><span data-stu-id="fc855-118">-MountPath</span></span>
<span data-ttu-id="fc855-119">Pfad im Container, in dem die von ShareName angegebene Freigabe verfügbar gemacht wird</span><span class="sxs-lookup"><span data-stu-id="fc855-119">Path in the container where the share specified by ShareName will be exposed</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc855-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fc855-120">-Name</span></span>
<span data-ttu-id="fc855-121">Der Bezeichner der Azure Storage-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="fc855-121">The identifier of the Azure Storage property.</span></span>
<span data-ttu-id="fc855-122">Muss innerhalb der Web App oder des Slot eindeutig sein</span><span class="sxs-lookup"><span data-stu-id="fc855-122">Must be unique within the Web App or Slot</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc855-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="fc855-123">-ShareName</span></span>
<span data-ttu-id="fc855-124">Name der Freigabe, die an den Container ge mountt werden soll</span><span class="sxs-lookup"><span data-stu-id="fc855-124">Name of the share to mount to the container</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc855-125">-Type</span><span class="sxs-lookup"><span data-stu-id="fc855-125">-Type</span></span>
<span data-ttu-id="fc855-126">Typ des Azure Storage-Kontos.</span><span class="sxs-lookup"><span data-stu-id="fc855-126">Type of Azure Storage account.</span></span>
<span data-ttu-id="fc855-127">Windows-Container unterstützen nur Azure-Dateien</span><span class="sxs-lookup"><span data-stu-id="fc855-127">Windows Containers only supports Azure Files</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.AzureStorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureFiles, AzureBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc855-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fc855-128">-Confirm</span></span>
<span data-ttu-id="fc855-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc855-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc855-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc855-130">-WhatIf</span></span>
<span data-ttu-id="fc855-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc855-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fc855-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc855-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc855-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc855-133">CommonParameters</span></span>
<span data-ttu-id="fc855-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc855-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc855-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc855-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc855-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fc855-136">INPUTS</span></span>

### <span data-ttu-id="fc855-137">Keine</span><span class="sxs-lookup"><span data-stu-id="fc855-137">None</span></span>

## <span data-ttu-id="fc855-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fc855-138">OUTPUTS</span></span>

### <span data-ttu-id="fc855-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="fc855-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span></span>

## <span data-ttu-id="fc855-140">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="fc855-140">NOTES</span></span>

## <span data-ttu-id="fc855-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="fc855-141">RELATED LINKS</span></span>
