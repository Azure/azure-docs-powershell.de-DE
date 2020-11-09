---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageFileServiceProperty.md
ms.openlocfilehash: e0e4eefaa652ca47f2d397acee1eeb0c8806de76
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302953"
---
# <span data-ttu-id="39ef5-101">Update-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="39ef5-101">Update-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="39ef5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="39ef5-102">SYNOPSIS</span></span>
<span data-ttu-id="39ef5-103">Ändert die Diensteigenschaften für den Azure Storage-Dateidienst.</span><span class="sxs-lookup"><span data-stu-id="39ef5-103">Modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="39ef5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="39ef5-104">SYNTAX</span></span>

### <span data-ttu-id="39ef5-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="39ef5-105">AccountName (Default)</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39ef5-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="39ef5-106">AccountObject</span></span>
```
Update-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount>
 [-EnableShareDeleteRetentionPolicy <Boolean>] [-ShareRetentionDays <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39ef5-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="39ef5-107">FileServicePropertiesResourceId</span></span>
```
Update-AzStorageFileServiceProperty [-ResourceId] <String> [-EnableShareDeleteRetentionPolicy <Boolean>]
 [-ShareRetentionDays <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39ef5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39ef5-108">DESCRIPTION</span></span>
<span data-ttu-id="39ef5-109">Das Cmdlet **Update-AzStorageFileServiceProperty** ändert die Diensteigenschaften für den Azure Storage-Dateidienst.</span><span class="sxs-lookup"><span data-stu-id="39ef5-109">The **Update-AzStorageFileServiceProperty** cmdlet modifies the service properties for the Azure Storage File service.</span></span>

## <span data-ttu-id="39ef5-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="39ef5-110">EXAMPLES</span></span>

### <span data-ttu-id="39ef5-111">Beispiel 1: Aktivieren von Dateifreigabe-softdelete</span><span class="sxs-lookup"><span data-stu-id="39ef5-111">Example 1: Enable File share softdelete</span></span>
```powershell
PS C:\> Update-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -EnableShareDeleteRetentionPolicy $true -ShareRetentionDays 5

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="39ef5-112">Dieser Befehl aktiviert Dateifreigabe-softdelete löschen mit Aufbewahrungs Tagen als 5</span><span class="sxs-lookup"><span data-stu-id="39ef5-112">This command enables File share softdelete delete with retention days as 5</span></span>

## <span data-ttu-id="39ef5-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="39ef5-113">PARAMETERS</span></span>

### <span data-ttu-id="39ef5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39ef5-114">-DefaultProfile</span></span>
<span data-ttu-id="39ef5-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="39ef5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39ef5-116">-EnableShareDeleteRetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="39ef5-116">-EnableShareDeleteRetentionPolicy</span></span>
<span data-ttu-id="39ef5-117">Aktivieren Sie Freigabe Aufbewahrungsrichtlinie für das Speicherkonto freigeben, indem Sie auf $true festlegen, Aufbewahrungsrichtlinie für Freigabe löschen deaktivieren, indem Sie auf $false festlegen.</span><span class="sxs-lookup"><span data-stu-id="39ef5-117">Enable share Delete Retention Policy for the storage account by set to $true, disable share Delete Retention Policy  by set to $false.</span></span>

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

### <span data-ttu-id="39ef5-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39ef5-118">-ResourceGroupName</span></span>
<span data-ttu-id="39ef5-119">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="39ef5-119">Resource Group Name.</span></span>

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

### <span data-ttu-id="39ef5-120">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="39ef5-120">-ResourceId</span></span>
<span data-ttu-id="39ef5-121">Geben Sie eine Ressourcen-ID des speicherkontos oder eine Ressourcen-ID für Dateidienst Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="39ef5-121">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

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

### <span data-ttu-id="39ef5-122">-ShareRetentionDays</span><span class="sxs-lookup"><span data-stu-id="39ef5-122">-ShareRetentionDays</span></span>
<span data-ttu-id="39ef5-123">Legt die Anzahl der Aufbewahrungstage für das Freigabe-DeleteRetentionPolicy fest.</span><span class="sxs-lookup"><span data-stu-id="39ef5-123">Sets the number of retention days for the share DeleteRetentionPolicy.</span></span>
<span data-ttu-id="39ef5-124">Der Wert sollte nur festgesetzt werden, wenn die Aufbewahrungsrichtlinie für Freigabe löschen aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="39ef5-124">The value should only be set when enable share Delete Retention Policy.</span></span>

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

### <span data-ttu-id="39ef5-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="39ef5-125">-StorageAccount</span></span>
<span data-ttu-id="39ef5-126">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="39ef5-126">Storage account object</span></span>

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

### <span data-ttu-id="39ef5-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="39ef5-127">-StorageAccountName</span></span>
<span data-ttu-id="39ef5-128">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="39ef5-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="39ef5-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="39ef5-129">-Confirm</span></span>
<span data-ttu-id="39ef5-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="39ef5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39ef5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39ef5-131">-WhatIf</span></span>
<span data-ttu-id="39ef5-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39ef5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39ef5-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39ef5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39ef5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39ef5-134">CommonParameters</span></span>
<span data-ttu-id="39ef5-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="39ef5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39ef5-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39ef5-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39ef5-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="39ef5-137">INPUTS</span></span>

### <span data-ttu-id="39ef5-138">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="39ef5-138">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="39ef5-139">System. String</span><span class="sxs-lookup"><span data-stu-id="39ef5-139">System.String</span></span>

## <span data-ttu-id="39ef5-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="39ef5-140">OUTPUTS</span></span>

### <span data-ttu-id="39ef5-141">Microsoft. Azure. Commands. Management. Storage. Models. PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="39ef5-141">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="39ef5-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="39ef5-142">NOTES</span></span>

## <span data-ttu-id="39ef5-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="39ef5-143">RELATED LINKS</span></span>
