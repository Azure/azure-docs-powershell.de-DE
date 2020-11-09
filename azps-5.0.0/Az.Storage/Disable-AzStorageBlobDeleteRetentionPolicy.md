---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobdeleteretentionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobDeleteRetentionPolicy.md
ms.openlocfilehash: f3891d30322a7c6577c14d43f7796a3242b53ecf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300412"
---
# <span data-ttu-id="79572-101">Disable-AzStorageBlobDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="79572-101">Disable-AzStorageBlobDeleteRetentionPolicy</span></span>

## <span data-ttu-id="79572-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79572-102">SYNOPSIS</span></span>
<span data-ttu-id="79572-103">Deaktivieren Sie die Aufbewahrungsrichtlinie für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="79572-103">Disable delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="79572-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79572-104">SYNTAX</span></span>

### <span data-ttu-id="79572-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="79572-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79572-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="79572-106">AccountObject</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79572-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="79572-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobDeleteRetentionPolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79572-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79572-108">DESCRIPTION</span></span>
<span data-ttu-id="79572-109">Das Cmdlet **Disable-AzStorageBlobDeleteRetentionPolicy** deaktiviert die Aufbewahrungsrichtlinie für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="79572-109">The **Disable-AzStorageBlobDeleteRetentionPolicy** cmdlet disables delete retention policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="79572-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79572-110">EXAMPLES</span></span>

### <span data-ttu-id="79572-111">Beispiel 1: Deaktivieren der Aufbewahrungsrichtlinie für den BLOB-Dienst</span><span class="sxs-lookup"><span data-stu-id="79572-111">Example 1: Disable delete retention policy for the Blob service</span></span>
```
C:\PS>Disable-AzStorageBlobDeleteRetentionPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -PassThru

Enabled Days
------- ----
  False
```

<span data-ttu-id="79572-112">Mit diesem Befehl wird die Aufbewahrungsrichtlinie für den BLOB-Dienst deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="79572-112">This command disables delete retention policy for the Blob service.</span></span>

## <span data-ttu-id="79572-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="79572-113">PARAMETERS</span></span>

### <span data-ttu-id="79572-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79572-114">-DefaultProfile</span></span>
<span data-ttu-id="79572-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="79572-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79572-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79572-116">-PassThru</span></span>
<span data-ttu-id="79572-117">ServiceProperties anzeigen</span><span class="sxs-lookup"><span data-stu-id="79572-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="79572-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79572-118">-ResourceGroupName</span></span>
<span data-ttu-id="79572-119">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="79572-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="79572-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="79572-120">-ResourceId</span></span>
<span data-ttu-id="79572-121">Geben Sie eine Ressourcen-ID des speicherkontos oder eine Ressourcen-ID für BLOB-Diensteigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="79572-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="79572-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="79572-122">-StorageAccount</span></span>
<span data-ttu-id="79572-123">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="79572-123">Storage account object</span></span>

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

### <span data-ttu-id="79572-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="79572-124">-StorageAccountName</span></span>
<span data-ttu-id="79572-125">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="79572-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="79572-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="79572-126">-Confirm</span></span>
<span data-ttu-id="79572-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="79572-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79572-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79572-128">-WhatIf</span></span>
<span data-ttu-id="79572-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="79572-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79572-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="79572-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79572-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79572-131">CommonParameters</span></span>
<span data-ttu-id="79572-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79572-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79572-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79572-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79572-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79572-134">INPUTS</span></span>

### <span data-ttu-id="79572-135">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="79572-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="79572-136">System. String</span><span class="sxs-lookup"><span data-stu-id="79572-136">System.String</span></span>

## <span data-ttu-id="79572-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79572-137">OUTPUTS</span></span>

### <span data-ttu-id="79572-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="79572-138">Microsoft.Azure.Commands.Management.Storage.Models.PSDeleteRetentionPolicy</span></span>

## <span data-ttu-id="79572-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="79572-139">NOTES</span></span>

## <span data-ttu-id="79572-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79572-140">RELATED LINKS</span></span>
