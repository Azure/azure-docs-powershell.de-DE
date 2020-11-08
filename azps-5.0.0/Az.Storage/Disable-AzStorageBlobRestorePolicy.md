---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/disable-azstorageblobrestorepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Disable-AzStorageBlobRestorePolicy.md
ms.openlocfilehash: 8e68400eeaedd6529ffc4069b36c6f73e25864f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175843"
---
# <span data-ttu-id="fb8fe-101">Disable-AzStorageBlobRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="fb8fe-101">Disable-AzStorageBlobRestorePolicy</span></span>

## <span data-ttu-id="fb8fe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb8fe-102">SYNOPSIS</span></span>
<span data-ttu-id="fb8fe-103">Deaktiviert die BLOB-Wiederherstellungsrichtlinie für ein Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="fb8fe-103">Disables Blob Restore Policy on a Storage account.</span></span>

## <span data-ttu-id="fb8fe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb8fe-104">SYNTAX</span></span>

### <span data-ttu-id="fb8fe-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="fb8fe-105">AccountName (Default)</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceGroupName] <String> [-StorageAccountName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb8fe-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="fb8fe-106">AccountObject</span></span>
```
Disable-AzStorageBlobRestorePolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fb8fe-107">BlobServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="fb8fe-107">BlobServicePropertiesResourceId</span></span>
```
Disable-AzStorageBlobRestorePolicy [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb8fe-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb8fe-108">DESCRIPTION</span></span>
<span data-ttu-id="fb8fe-109">Das Cmdlet **Disable-AzStorageBlobRestorePolicy** deaktiviert die BLOB-Wiederherstellungsrichtlinie für den Azure Storage-BLOB-Dienst.</span><span class="sxs-lookup"><span data-stu-id="fb8fe-109">The **Disable-AzStorageBlobRestorePolicy** cmdlet disables Blob Restore Policy for the Azure Storage Blob service.</span></span>

## <span data-ttu-id="fb8fe-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb8fe-110">EXAMPLES</span></span>

### <span data-ttu-id="fb8fe-111">Beispiel 1: deaktiviert die BLOB-Wiederherstellungsrichtlinie für den Azure Storage-BLOB-Dienst auf einem Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="fb8fe-111">Example 1: Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account</span></span>
```powershell
PS C:\> Disable-AzStorageBlobRestorePolicy -ResourceGroupName "myresourcegoup" -StorageAccountName "mystorageaccount"
```

<span data-ttu-id="fb8fe-112">Mit diesem Befehl wird die BLOB-Wiederherstellungsrichtlinie für den Azure Storage-BLOB-Dienst auf einem Speicherkonto deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="fb8fe-112">This command Disables Blob Restore Policy for the Azure Storage Blob service on a Storage account.</span></span>

## <span data-ttu-id="fb8fe-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb8fe-113">PARAMETERS</span></span>

### <span data-ttu-id="fb8fe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb8fe-114">-DefaultProfile</span></span>
<span data-ttu-id="fb8fe-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fb8fe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb8fe-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fb8fe-116">-PassThru</span></span>
<span data-ttu-id="fb8fe-117">ServiceProperties anzeigen</span><span class="sxs-lookup"><span data-stu-id="fb8fe-117">Display ServiceProperties</span></span>

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

### <span data-ttu-id="fb8fe-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb8fe-118">-ResourceGroupName</span></span>
<span data-ttu-id="fb8fe-119">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fb8fe-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="fb8fe-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fb8fe-120">-ResourceId</span></span>
<span data-ttu-id="fb8fe-121">Geben Sie eine Ressourcen-ID des speicherkontos oder eine Ressourcen-ID für BLOB-Diensteigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="fb8fe-121">Input a Storage account Resource Id, or a Blob service properties Resource Id.</span></span>

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

### <span data-ttu-id="fb8fe-122">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="fb8fe-122">-StorageAccount</span></span>
<span data-ttu-id="fb8fe-123">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="fb8fe-123">Storage account object</span></span>

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

### <span data-ttu-id="fb8fe-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fb8fe-124">-StorageAccountName</span></span>
<span data-ttu-id="fb8fe-125">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="fb8fe-125">Storage Account Name.</span></span>

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

### <span data-ttu-id="fb8fe-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fb8fe-126">-Confirm</span></span>
<span data-ttu-id="fb8fe-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fb8fe-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb8fe-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb8fe-128">-WhatIf</span></span>
<span data-ttu-id="fb8fe-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fb8fe-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb8fe-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fb8fe-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb8fe-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb8fe-131">CommonParameters</span></span>
<span data-ttu-id="fb8fe-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb8fe-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb8fe-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb8fe-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb8fe-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb8fe-134">INPUTS</span></span>

### <span data-ttu-id="fb8fe-135">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fb8fe-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="fb8fe-136">System. String</span><span class="sxs-lookup"><span data-stu-id="fb8fe-136">System.String</span></span>

## <span data-ttu-id="fb8fe-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb8fe-137">OUTPUTS</span></span>

### <span data-ttu-id="fb8fe-138">Microsoft. Azure. Commands. Management. Storage. Models. PSRestorePolicy</span><span class="sxs-lookup"><span data-stu-id="fb8fe-138">Microsoft.Azure.Commands.Management.Storage.Models.PSRestorePolicy</span></span>

## <span data-ttu-id="fb8fe-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb8fe-139">NOTES</span></span>

## <span data-ttu-id="fb8fe-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb8fe-140">RELATED LINKS</span></span>
