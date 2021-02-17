---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
ms.openlocfilehash: e0e4eefaa652ca47f2d397acee1eeb0c8806de76
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164700"
---
# <span data-ttu-id="d47f9-101">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="d47f9-101">Update-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="d47f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d47f9-102">SYNOPSIS</span></span>
<span data-ttu-id="d47f9-103">Ändert die Diensteigenschaften für den Azure Storage File-Dienst.</span><span class="sxs-lookup"><span data-stu-id="d47f9-103">Modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="d47f9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d47f9-104">SYNTAX</span></span>

### <span data-ttu-id="d47f9-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d47f9-105">AccountName (Default)</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d47f9-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="d47f9-106">AccountObject</span></span>
```
Update-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d47f9-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="d47f9-107">FileServicePropertiesResourceId</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceId] <String> [-EnableShareDeleteRetentionPolicy <Boolean>]
 [-ShareRetentionDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d47f9-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d47f9-108">DESCRIPTION</span></span>
<span data-ttu-id="d47f9-109">Das **Cmdlet "Update-AzStorageFileServiceProperty"** ändert die Diensteigenschaften für den Azure Storage File-Dienst.</span><span class="sxs-lookup"><span data-stu-id="d47f9-109">The **Update-AzStorageFileServiceProperty** cmdlet modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="d47f9-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d47f9-110">EXAMPLES</span></span>

### <span data-ttu-id="d47f9-111">Beispiel 1: Aktivieren der Softdelete für die Dateifreigabe</span><span class="sxs-lookup"><span data-stu-id="d47f9-111">Example 1: Enable File share softdelete</span></span>
```powershell
PS C:\> Update-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableShareDeleteRetentionPolicy $true -ShareRetentionDays 5

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="d47f9-112">Dieser Befehl aktiviert das softdelete Löschen der Dateifreigabe mit Aufbewahrungstagen als 5.</span><span class="sxs-lookup"><span data-stu-id="d47f9-112">This command enables File share softdelete delete with retention days as 5</span></span>

## <span data-ttu-id="d47f9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d47f9-113">PARAMETERS</span></span>

### <span data-ttu-id="d47f9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d47f9-114">-DefaultProfile</span></span>
<span data-ttu-id="d47f9-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d47f9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d47f9-116">-EnableShareDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="d47f9-116">-EnableShareDeleteRetentionPolicy</span></span>
<span data-ttu-id="d47f9-117">Aktivieren Sie die Freigabelöschaufbewahrungsrichtlinie für das Speicherkonto, indem Sie auf $true, die Aufbewahrungsrichtlinie für das Teilen deaktivieren, indem Sie sie auf $false.</span><span class="sxs-lookup"><span data-stu-id="d47f9-117">Enable share Delete Retention Policy for the storage account by set to $true, disable share Delete Retention Policy  by set to $false.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d47f9-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d47f9-118">-ResourceGroupName</span></span>
<span data-ttu-id="d47f9-119">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="d47f9-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="d47f9-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d47f9-120">-ResourceId</span></span>
<span data-ttu-id="d47f9-121">Geben Sie eine Ressourcen-ID des Speicherkontos oder eine Dateidiensteigenschaften-Ressourcen-ID ein.</span><span class="sxs-lookup"><span data-stu-id="d47f9-121">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

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

### <span data-ttu-id="d47f9-122">-ShareRetentionDays</span><span class="sxs-lookup"><span data-stu-id="d47f9-122">-ShareRetentionDays</span></span>
<span data-ttu-id="d47f9-123">Legt die Anzahl der Aufbewahrungstage für "DeleteRetentionPolicy" für die Freigabe fest.</span><span class="sxs-lookup"><span data-stu-id="d47f9-123">Sets the number of retention days for the share DeleteRetentionPolicy.</span></span>
<span data-ttu-id="d47f9-124">Der Wert sollte nur festgelegt werden, wenn die Freigabe-Löschaufbewahrungsrichtlinie aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d47f9-124">The value should only be set when enable share Delete Retention Policy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: Days, RetentionDays

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d47f9-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="d47f9-125">-StorageAccount</span></span>
<span data-ttu-id="d47f9-126">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="d47f9-126">Storage account object</span></span>

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

### <span data-ttu-id="d47f9-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d47f9-127">-StorageAccountName</span></span>
<span data-ttu-id="d47f9-128">Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="d47f9-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="d47f9-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d47f9-129">-Confirm</span></span>
<span data-ttu-id="d47f9-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d47f9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d47f9-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d47f9-131">-WhatIf</span></span>
<span data-ttu-id="d47f9-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d47f9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d47f9-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d47f9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d47f9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d47f9-134">CommonParameters</span></span>
<span data-ttu-id="d47f9-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d47f9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d47f9-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d47f9-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d47f9-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d47f9-137">INPUTS</span></span>

### <span data-ttu-id="d47f9-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="d47f9-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="d47f9-139">System.String</span><span class="sxs-lookup"><span data-stu-id="d47f9-139">System.String</span></span>

## <span data-ttu-id="d47f9-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d47f9-140">OUTPUTS</span></span>

### <span data-ttu-id="d47f9-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="d47f9-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="d47f9-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d47f9-142">NOTES</span></span>

## <span data-ttu-id="d47f9-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d47f9-143">RELATED LINKS</span></span>
