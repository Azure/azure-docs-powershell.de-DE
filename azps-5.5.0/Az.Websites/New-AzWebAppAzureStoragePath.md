---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappazurestoragepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppAzureStoragePath.md
ms.openlocfilehash: 5571add1c12ac40279531274b47acfe67fc19734
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149684"
---
# <span data-ttu-id="16b35-101">New-AzWebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="16b35-101">New-AzWebAppAzureStoragePath</span></span>

## <span data-ttu-id="16b35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16b35-102">SYNOPSIS</span></span>
<span data-ttu-id="16b35-103">Erstellt ein Objekt, das einen Azure -Speicherpfad darstellt, der in einer Web App bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="16b35-103">Creates an object that represents an Azure Storage path to be mounted in a Web App.</span></span> <span data-ttu-id="16b35-104">Er soll als Parameter (-AzureStoragePath) zum Set-AzWebApp und Set-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="16b35-104">It is meant to be used as a parameter (-AzureStoragePath) to Set-AzWebApp and Set-AzWebAppSlot</span></span>

## <span data-ttu-id="16b35-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16b35-105">SYNTAX</span></span>

```
New-AzWebAppAzureStoragePath -Name <String> -Type <AzureStorageType> -AccountName <String> -ShareName <String>
 -AccessKey <String> -MountPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16b35-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16b35-106">DESCRIPTION</span></span>
<span data-ttu-id="16b35-107">Erstellt ein Objekt, das einen Azure -Speicherpfad repräsentiert, der in einer Web App bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="16b35-107">Creates an object that represent an Azure Storage path to be mounted inside a Web App.</span></span>

## <span data-ttu-id="16b35-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="16b35-108">EXAMPLES</span></span>

### <span data-ttu-id="16b35-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="16b35-109">Example 1</span></span>
```powershell
PS C:\> $storagePath1 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount1" -AccountName "myaccount.files.core.windows.net" -Type AzureFiles -ShareName "someShareName" -AccessKey "some access key"
-MountPath "C:\myFolderInsideTheContainerWebApp" 

PS C:\> $storagePath2 = New-AzWebAppAzureStoragePath -Name "RemoteStorageAccount2" -AccountName "myaccount2.files.core.windows.net" -Type AzureFiles -ShareName "someShareName2" -AccessKey "some access key 2"
-MountPath "C:\myFolderInsideTheContainerWebApp2" 

PS C:\> Set-AzWebApp -ResourceGroup myresourcegroup -Name myapp -AzureStoragePath $storagepath1, $storagePath2
```

## <span data-ttu-id="16b35-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16b35-110">PARAMETERS</span></span>

### <span data-ttu-id="16b35-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="16b35-111">-AccessKey</span></span>
<span data-ttu-id="16b35-112">Zugriffsschlüssel für das Azure Storage-Konto</span><span class="sxs-lookup"><span data-stu-id="16b35-112">Access key to the Azure Storage account</span></span>

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

### <span data-ttu-id="16b35-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="16b35-113">-AccountName</span></span>
<span data-ttu-id="16b35-114">Azure Storage-Kontoname.</span><span class="sxs-lookup"><span data-stu-id="16b35-114">Azure Storage account name.</span></span>
<span data-ttu-id="16b35-115">Beispiel: myfilestorageaccount.file.core.windows.net</span><span class="sxs-lookup"><span data-stu-id="16b35-115">E.g.: myfilestorageaccount.file.core.windows.net</span></span>

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

### <span data-ttu-id="16b35-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16b35-116">-DefaultProfile</span></span>
<span data-ttu-id="16b35-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="16b35-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16b35-118">-MountPath</span><span class="sxs-lookup"><span data-stu-id="16b35-118">-MountPath</span></span>
<span data-ttu-id="16b35-119">Pfad im Container, in dem die von ShareName angegebene Freigabe verfügbar gemacht wird</span><span class="sxs-lookup"><span data-stu-id="16b35-119">Path in the container where the share specified by ShareName will be exposed</span></span>

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

### <span data-ttu-id="16b35-120">-Name</span><span class="sxs-lookup"><span data-stu-id="16b35-120">-Name</span></span>
<span data-ttu-id="16b35-121">Der Bezeichner der Azure Storage-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="16b35-121">The identifier of the Azure Storage property.</span></span>
<span data-ttu-id="16b35-122">Muss innerhalb der Web App oder des Slot eindeutig sein</span><span class="sxs-lookup"><span data-stu-id="16b35-122">Must be unique within the Web App or Slot</span></span>

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

### <span data-ttu-id="16b35-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="16b35-123">-ShareName</span></span>
<span data-ttu-id="16b35-124">Name der Freigabe, die im Container angezeigt werden soll</span><span class="sxs-lookup"><span data-stu-id="16b35-124">Name of the share to mount to the container</span></span>

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

### <span data-ttu-id="16b35-125">-Type</span><span class="sxs-lookup"><span data-stu-id="16b35-125">-Type</span></span>
<span data-ttu-id="16b35-126">Typ des Azure Storage-Kontos.</span><span class="sxs-lookup"><span data-stu-id="16b35-126">Type of Azure Storage account.</span></span>
<span data-ttu-id="16b35-127">Windows Containers unterstützt nur Azure-Dateien.</span><span class="sxs-lookup"><span data-stu-id="16b35-127">Windows Containers only supports Azure Files</span></span>

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

### <span data-ttu-id="16b35-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="16b35-128">-Confirm</span></span>
<span data-ttu-id="16b35-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="16b35-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16b35-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="16b35-130">-WhatIf</span></span>
<span data-ttu-id="16b35-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16b35-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16b35-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="16b35-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16b35-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16b35-133">CommonParameters</span></span>
<span data-ttu-id="16b35-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16b35-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16b35-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16b35-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16b35-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="16b35-136">INPUTS</span></span>

### <span data-ttu-id="16b35-137">Keine</span><span class="sxs-lookup"><span data-stu-id="16b35-137">None</span></span>

## <span data-ttu-id="16b35-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="16b35-138">OUTPUTS</span></span>

### <span data-ttu-id="16b35-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span><span class="sxs-lookup"><span data-stu-id="16b35-139">Microsoft.Azure.Commands.WebApps.Models.WebAppAzureStoragePath</span></span>

## <span data-ttu-id="16b35-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="16b35-140">NOTES</span></span>

## <span data-ttu-id="16b35-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="16b35-141">RELATED LINKS</span></span>
