---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/new-azurermmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/New-AzureRmMediaServiceStorageConfig.md
ms.openlocfilehash: 7296d744749dd037c10d0d4d5ee2b0461a55b794
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663246"
---
# <span data-ttu-id="868e7-101">New-AzureRmMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="868e7-101">New-AzureRmMediaServiceStorageConfig</span></span>

## <span data-ttu-id="868e7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="868e7-102">SYNOPSIS</span></span>
<span data-ttu-id="868e7-103">Erstellen Sie eine Speicherkonto Konfiguration für die Media Service-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="868e7-103">Create a storage account configuration for the media service cmdlets.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="868e7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="868e7-104">SYNTAX</span></span>

```
New-AzureRmMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="868e7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="868e7-105">DESCRIPTION</span></span>
<span data-ttu-id="868e7-106">Das Cmdlet **New-AzureRmMediaServiceStorageConfig** erstellt eine Speicherkonto Konfiguration für die Mediendienst-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="868e7-106">The **New-AzureRmMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="868e7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="868e7-107">EXAMPLES</span></span>

### <span data-ttu-id="868e7-108">Beispiel 1: Erstellen einer Speicherkonto Konfiguration für die Media Service-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="868e7-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzureRmStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzureRmMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="868e7-109">Der erste Befehl erstellt ein Speicherkonto Objekt mithilfe des Cmdlets **New-AzureRmStorageAccount** .</span><span class="sxs-lookup"><span data-stu-id="868e7-109">The first command creates a storage account object by using **the New-AzureRmStorageAccount** cmdlet.</span></span>
<span data-ttu-id="868e7-110">Der Befehl benennt dieses Speicherkonto Storage1 und der Typ hat den Namen Standard_GRS und speichert das Ergebnis in der Variablen mit dem Namen $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="868e7-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>

<span data-ttu-id="868e7-111">Mit dem zweiten Befehl wird ein Speicher Konfigurationsobjekt als das primäre Speicherkonto erstellt, das dem Mediendienst unter Verwendung der Speicherkonto-ID-Informationen zugeordnet ist, die in der $StorageAccount Variablen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="868e7-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="868e7-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="868e7-112">PARAMETERS</span></span>

### <span data-ttu-id="868e7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="868e7-113">-DefaultProfile</span></span>
<span data-ttu-id="868e7-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="868e7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="868e7-115">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="868e7-115">-IsPrimary</span></span>
<span data-ttu-id="868e7-116">Gibt an, dass das Cmdlet das Speicherkonto als primären Speicher für den Mediendienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="868e7-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="868e7-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="868e7-117">-StorageAccountId</span></span>
<span data-ttu-id="868e7-118">Gibt die ID des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="868e7-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="868e7-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="868e7-119">-Confirm</span></span>
<span data-ttu-id="868e7-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="868e7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="868e7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="868e7-121">-WhatIf</span></span>
<span data-ttu-id="868e7-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="868e7-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="868e7-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="868e7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="868e7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="868e7-124">CommonParameters</span></span>
<span data-ttu-id="868e7-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="868e7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="868e7-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="868e7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="868e7-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="868e7-127">INPUTS</span></span>

### <span data-ttu-id="868e7-128">Keine</span><span class="sxs-lookup"><span data-stu-id="868e7-128">None</span></span>
<span data-ttu-id="868e7-129">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="868e7-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="868e7-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="868e7-130">OUTPUTS</span></span>

### <span data-ttu-id="868e7-131">Microsoft. Azure. Commands. Media. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="868e7-131">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="868e7-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="868e7-132">NOTES</span></span>

## <span data-ttu-id="868e7-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="868e7-133">RELATED LINKS</span></span>

[<span data-ttu-id="868e7-134">Synchronisieren-AzureRmMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="868e7-134">Sync-AzureRmMediaServiceStorageKeys</span></span>](./Sync-AzureRmMediaServiceStorageKeys.md)


