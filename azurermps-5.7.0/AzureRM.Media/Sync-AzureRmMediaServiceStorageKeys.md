---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/sync-azurermmediaservicestoragekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Sync-AzureRmMediaServiceStorageKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Sync-AzureRmMediaServiceStorageKeys.md
ms.openlocfilehash: 1f61718a6812977b86e32b12cd8ce8bdafbde207
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496485"
---
# <span data-ttu-id="364d1-101">Sync-AzureRmMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="364d1-101">Sync-AzureRmMediaServiceStorageKeys</span></span>

## <span data-ttu-id="364d1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="364d1-102">SYNOPSIS</span></span>
<span data-ttu-id="364d1-103">Synchronisiert speicherkontoschlüssel für ein Speicherkonto, das dem Mediendienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="364d1-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="364d1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="364d1-104">SYNTAX</span></span>

```
Sync-AzureRmMediaServiceStorageKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="364d1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="364d1-105">DESCRIPTION</span></span>
<span data-ttu-id="364d1-106">Das Cmdlet " **Sync-AzureRmMediaServiceStorageKeys** " synchronisiert speicherkontoschlüssel für ein Speicherkonto, das dem Mediendienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="364d1-106">The **Sync-AzureRmMediaServiceStorageKeys** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="364d1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="364d1-107">EXAMPLES</span></span>

### <span data-ttu-id="364d1-108">Beispiel 1: Synchronisieren von Speicherkonto Schlüsseln für ein Speicherkonto, das dem Mediendienst zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="364d1-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzureRmStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzureRmMediaServiceStorageKeys -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="364d1-109">Der erste Befehl verwendet das Get-AzureRmStorageAccount-Cmdlet zum Abrufen des speicherkontos mit dem Namen Storage135, das zu ResourceGroup001 gehört, und speichert das Ergebnis in der Variablen mit dem Namen $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="364d1-109">The first command uses the Get-AzureRmStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>

<span data-ttu-id="364d1-110">Der zweite Befehl synchronisiert die speicherkontoschlüssel für den Mediendienst mit dem Namen MediaService001 mithilfe der **ID** -Eigenschaft, die in der $StorageAccount-Variablen enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="364d1-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="364d1-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="364d1-111">PARAMETERS</span></span>

### <span data-ttu-id="364d1-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="364d1-112">-AccountName</span></span>
<span data-ttu-id="364d1-113">Gibt den Namen des Medien Diensts an, den dieses Cmdlet synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="364d1-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="364d1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="364d1-114">-DefaultProfile</span></span>
<span data-ttu-id="364d1-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="364d1-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="364d1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="364d1-116">-ResourceGroupName</span></span>
<span data-ttu-id="364d1-117">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="364d1-117">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="364d1-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="364d1-118">-StorageAccountId</span></span>
<span data-ttu-id="364d1-119">Gibt die dem Mediendienst Konto zugeordnete Speicherkonto-ID an.</span><span class="sxs-lookup"><span data-stu-id="364d1-119">Specifies the storage account ID associated with the media service account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="364d1-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="364d1-120">-Confirm</span></span>
<span data-ttu-id="364d1-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="364d1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="364d1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="364d1-122">-WhatIf</span></span>
<span data-ttu-id="364d1-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="364d1-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="364d1-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="364d1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="364d1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="364d1-125">CommonParameters</span></span>
<span data-ttu-id="364d1-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="364d1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="364d1-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="364d1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="364d1-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="364d1-128">INPUTS</span></span>

### <span data-ttu-id="364d1-129">Keine</span><span class="sxs-lookup"><span data-stu-id="364d1-129">None</span></span>
<span data-ttu-id="364d1-130">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="364d1-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="364d1-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="364d1-131">OUTPUTS</span></span>

### <span data-ttu-id="364d1-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="364d1-132">System.Boolean</span></span>

## <span data-ttu-id="364d1-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="364d1-133">NOTES</span></span>

## <span data-ttu-id="364d1-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="364d1-134">RELATED LINKS</span></span>

