---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: 8e68400eeaedd6529ffc4069b36c6f73e25864f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100156108"
---
# <span data-ttu-id="b09bd-101">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="b09bd-101">Disable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="b09bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b09bd-102">SYNOPSIS</span></span>
<span data-ttu-id="b09bd-103">Deaktiviert die Blob Restore-Richtlinie für ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="b09bd-103">Disables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="b09bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b09bd-104">SYNTAX</span></span>

### <span data-ttu-id="b09bd-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b09bd-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b09bd-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="b09bd-106">AccountObject</span></span>
```
Disable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b09bd-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="b09bd-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b09bd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b09bd-108">DESCRIPTION</span></span>
<span data-ttu-id="b09bd-109">Das **Cmdlet "Disable-AzStorageBlobRestorePolicy"** deaktiviert die Blob Restore Policy für den Azure Storage BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="b09bd-109">The **Disable-AzStorageBlobRestorePolicy** cmdlet disables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="b09bd-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b09bd-110">EXAMPLES</span></span>

### <span data-ttu-id="b09bd-111">Beispiel 1: Deaktiviert die Blob Restore Policy für den Azure Storage -BLOB-Dienst für ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="b09bd-111">Example 1: Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Disable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"
```

<span data-ttu-id="b09bd-112">Mit diesem Befehl wird die Blob Restore Policy für den Azure Storage -BLOB-Dienst für ein Speicherkonto deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b09bd-112">This command Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account.</span></span>

## <span data-ttu-id="b09bd-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b09bd-113">PARAMETERS</span></span>

### <span data-ttu-id="b09bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b09bd-114">-DefaultProfile</span></span>
<span data-ttu-id="b09bd-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b09bd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b09bd-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b09bd-116">-PassThru</span></span>
<span data-ttu-id="b09bd-117">Anzeigen von ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="b09bd-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="b09bd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b09bd-118">-ResourceGroupName</span></span>
<span data-ttu-id="b09bd-119">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="b09bd-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="b09bd-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b09bd-120">-ResourceId</span></span>
<span data-ttu-id="b09bd-121">Geben Sie die Ressourcen-ID eines Speicherkontos oder eine Blob-Diensteigenschaften-Ressourcen-ID ein.</span><span class="sxs-lookup"><span data-stu-id="b09bd-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="b09bd-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="b09bd-122">-StorageAccount</span></span>
<span data-ttu-id="b09bd-123">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="b09bd-123">Storage account object</span></span>

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

### <span data-ttu-id="b09bd-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b09bd-124">-StorageAccountName</span></span>
<span data-ttu-id="b09bd-125">Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="b09bd-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="b09bd-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b09bd-126">-Confirm</span></span>
<span data-ttu-id="b09bd-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b09bd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b09bd-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b09bd-128">-WhatIf</span></span>
<span data-ttu-id="b09bd-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b09bd-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b09bd-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b09bd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b09bd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b09bd-131">CommonParameters</span></span>
<span data-ttu-id="b09bd-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b09bd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b09bd-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b09bd-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b09bd-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b09bd-134">INPUTS</span></span>

### <span data-ttu-id="b09bd-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b09bd-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="b09bd-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b09bd-136">System.String</span></span>

## <span data-ttu-id="b09bd-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b09bd-137">OUTPUTS</span></span>

### <span data-ttu-id="b09bd-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="b09bd-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="b09bd-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b09bd-139">NOTES</span></span>

## <span data-ttu-id="b09bd-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b09bd-140">RELATED LINKS</span></span>
