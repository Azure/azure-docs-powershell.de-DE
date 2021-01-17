---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: f3891d30322a7c6577c14d43f7796a3242b53ecf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304344"
---
# <span data-ttu-id="2fc07-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2fc07-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="2fc07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fc07-102">SYNOPSIS</span></span>
<span data-ttu-id="2fc07-103">Deaktivieren Sie die Löschaufbewahrungsrichtlinie für den Azure Storage Blob-Dienst.</span><span class="sxs-lookup"><span data-stu-id="2fc07-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="2fc07-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2fc07-104">SYNTAX</span></span>

### <span data-ttu-id="2fc07-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="2fc07-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc07-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="2fc07-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2fc07-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="2fc07-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fc07-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2fc07-108">DESCRIPTION</span></span>
<span data-ttu-id="2fc07-109">Das **Cmdlet "Disable-AzStorageBlobDeleteRetentionPolicy"** deaktiviert die Löschaufbewahrungsrichtlinie für den Azure Storage Blob-Dienst.</span><span class="sxs-lookup"><span data-stu-id="2fc07-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="2fc07-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2fc07-110">EXAMPLES</span></span>

### <span data-ttu-id="2fc07-111">Beispiel 1: Deaktivieren der Löschaufbewahrungsrichtlinie für den Blob-Dienst</span><span class="sxs-lookup"><span data-stu-id="2fc07-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="2fc07-112">Dieser Befehl deaktiviert die Löschaufbewahrungsrichtlinie für den Blob-Dienst.</span><span class="sxs-lookup"><span data-stu-id="2fc07-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="2fc07-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2fc07-113">PARAMETERS</span></span>

### <span data-ttu-id="2fc07-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc07-114">-DefaultProfile</span></span>
<span data-ttu-id="2fc07-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2fc07-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fc07-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2fc07-116">-PassThru</span></span>
<span data-ttu-id="2fc07-117">Anzeigen von ServiceProperties</span><span class="sxs-lookup"><span data-stu-id="2fc07-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="2fc07-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fc07-118">-ResourceGroupName</span></span>
<span data-ttu-id="2fc07-119">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="2fc07-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="2fc07-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fc07-120">-ResourceId</span></span>
<span data-ttu-id="2fc07-121">Geben Sie die Ressourcen-ID eines Speicherkontos oder eine Blob-Diensteigenschaften-Ressourcen-ID ein.</span><span class="sxs-lookup"><span data-stu-id="2fc07-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="2fc07-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="2fc07-122">-StorageAccount</span></span>
<span data-ttu-id="2fc07-123">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="2fc07-123">Storage account object</span></span>

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

### <span data-ttu-id="2fc07-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2fc07-124">-StorageAccountName</span></span>
<span data-ttu-id="2fc07-125">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="2fc07-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="2fc07-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2fc07-126">-Confirm</span></span>
<span data-ttu-id="2fc07-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2fc07-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fc07-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="2fc07-128">-WhatIf</span></span>
<span data-ttu-id="2fc07-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2fc07-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fc07-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2fc07-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fc07-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc07-131">CommonParameters</span></span>
<span data-ttu-id="2fc07-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fc07-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc07-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fc07-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc07-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2fc07-134">INPUTS</span></span>

### <span data-ttu-id="2fc07-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2fc07-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="2fc07-136">System.String</span><span class="sxs-lookup"><span data-stu-id="2fc07-136">System.String</span></span>

## <span data-ttu-id="2fc07-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2fc07-137">OUTPUTS</span></span>

### <span data-ttu-id="2fc07-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="2fc07-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="2fc07-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="2fc07-139">NOTES</span></span>

## <span data-ttu-id="2fc07-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="2fc07-140">RELATED LINKS</span></span>
