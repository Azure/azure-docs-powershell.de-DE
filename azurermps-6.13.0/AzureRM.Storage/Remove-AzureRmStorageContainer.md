---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainer.md
ms.openlocfilehash: 089451a0a0aae399a18296fbf4982724b35d432e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664793"
---
# <span data-ttu-id="3c6e1-101">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="3c6e1-101">Remove-AzureRmStorageContainer</span></span>

## <span data-ttu-id="3c6e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3c6e1-102">SYNOPSIS</span></span>
<span data-ttu-id="3c6e1-103">Entfernt einen BLOB-Speichercontainer</span><span class="sxs-lookup"><span data-stu-id="3c6e1-103">Removes a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c6e1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c6e1-104">SYNTAX</span></span>

### <span data-ttu-id="3c6e1-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="3c6e1-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c6e1-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="3c6e1-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c6e1-107">Containerobject</span><span class="sxs-lookup"><span data-stu-id="3c6e1-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c6e1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c6e1-108">DESCRIPTION</span></span>
<span data-ttu-id="3c6e1-109">Das Cmdlet " **Remove-AzureRmStorageContainer** " entfernt einen Speicher-BLOB-Container</span><span class="sxs-lookup"><span data-stu-id="3c6e1-109">The **Remove-AzureRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="3c6e1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3c6e1-110">EXAMPLES</span></span>

### <span data-ttu-id="3c6e1-111">Beispiel 1: Entfernen eines Speicher-BLOB-Containers mit dem Namen des speicherkontos und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="3c6e1-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="3c6e1-112">Dieser Befehl entfernt einen Speicher-BLOB-Container mit dem Namen des speicherkontos und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="3c6e1-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="3c6e1-113">Beispiel 2: Entfernen eines Speicher-BLOB-Containers mit dem Speicherkonto Objekt und dem Containernamen</span><span class="sxs-lookup"><span data-stu-id="3c6e1-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="3c6e1-114">Dieser Befehl entfernt einen Speicher-BLOB-Container mit dem Speicherkonto Objekt und dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="3c6e1-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="3c6e1-115">Beispiel 3: Entfernen aller BLOB-Speichercontainer in einem Speicherkonto mit Pipeline</span><span class="sxs-lookup"><span data-stu-id="3c6e1-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzureRmStorageContainer -Force
```

<span data-ttu-id="3c6e1-116">Dieser Befehl entfernt alle Speicher-BLOB-Container in einem Speicherkonto mit Pipeline.</span><span class="sxs-lookup"><span data-stu-id="3c6e1-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="3c6e1-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c6e1-117">PARAMETERS</span></span>

### <span data-ttu-id="3c6e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c6e1-118">-DefaultProfile</span></span>
<span data-ttu-id="3c6e1-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3c6e1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6e1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3c6e1-120">-Force</span></span>
<span data-ttu-id="3c6e1-121">Erzwingen des Entfernens des Containers und des gesamten Inhalts</span><span class="sxs-lookup"><span data-stu-id="3c6e1-121">Force to remove the container and all content in it</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6e1-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3c6e1-122">-InputObject</span></span>
<span data-ttu-id="3c6e1-123">Speichercontainer Objekt</span><span class="sxs-lookup"><span data-stu-id="3c6e1-123">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6e1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3c6e1-124">-Name</span></span>
<span data-ttu-id="3c6e1-125">Container Name</span><span class="sxs-lookup"><span data-stu-id="3c6e1-125">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6e1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c6e1-126">-PassThru</span></span>
<span data-ttu-id="3c6e1-127">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="3c6e1-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6e1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c6e1-128">-ResourceGroupName</span></span>
<span data-ttu-id="3c6e1-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3c6e1-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6e1-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="3c6e1-130">-StorageAccount</span></span>
<span data-ttu-id="3c6e1-131">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="3c6e1-131">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6e1-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3c6e1-132">-StorageAccountName</span></span>
<span data-ttu-id="3c6e1-133">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="3c6e1-133">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c6e1-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3c6e1-134">-Confirm</span></span>
<span data-ttu-id="3c6e1-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3c6e1-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6e1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c6e1-136">-WhatIf</span></span>
<span data-ttu-id="3c6e1-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3c6e1-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3c6e1-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3c6e1-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c6e1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c6e1-139">CommonParameters</span></span>
<span data-ttu-id="3c6e1-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c6e1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c6e1-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c6e1-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c6e1-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3c6e1-142">INPUTS</span></span>

### <span data-ttu-id="3c6e1-143">System. String</span><span class="sxs-lookup"><span data-stu-id="3c6e1-143">System.String</span></span>

## <span data-ttu-id="3c6e1-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3c6e1-144">OUTPUTS</span></span>

### <span data-ttu-id="3c6e1-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="3c6e1-145">System.Object</span></span>

## <span data-ttu-id="3c6e1-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="3c6e1-146">NOTES</span></span>

## <span data-ttu-id="3c6e1-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3c6e1-147">RELATED LINKS</span></span>
