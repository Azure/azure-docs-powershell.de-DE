---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
ms.openlocfilehash: 8fb6e4a683decc8b5615a7cf0c8088681578f8ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93650601"
---
# <span data-ttu-id="04a00-101">New-AzMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="04a00-101">New-AzMediaServiceStorageConfig</span></span>

## <span data-ttu-id="04a00-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="04a00-102">SYNOPSIS</span></span>
<span data-ttu-id="04a00-103">Erstellen Sie eine Speicherkonto Konfiguration für die Media Service-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="04a00-103">Create a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="04a00-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="04a00-104">SYNTAX</span></span>

```
New-AzMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04a00-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04a00-105">DESCRIPTION</span></span>
<span data-ttu-id="04a00-106">Das Cmdlet **New-AzMediaServiceStorageConfig** erstellt eine Speicherkonto Konfiguration für die Mediendienst-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="04a00-106">The **New-AzMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="04a00-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="04a00-107">EXAMPLES</span></span>

### <span data-ttu-id="04a00-108">Beispiel 1: Erstellen einer Speicherkonto Konfiguration für die Media Service-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="04a00-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="04a00-109">Der erste Befehl erstellt ein Speicherkonto Objekt mithilfe des Cmdlets **New-AzStorageAccount** .</span><span class="sxs-lookup"><span data-stu-id="04a00-109">The first command creates a storage account object by using **the New-AzStorageAccount** cmdlet.</span></span>
<span data-ttu-id="04a00-110">Der Befehl benennt dieses Speicherkonto Storage1 und der Typ hat den Namen Standard_GRS und speichert das Ergebnis in der Variablen mit dem Namen $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="04a00-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="04a00-111">Mit dem zweiten Befehl wird ein Speicher Konfigurationsobjekt als das primäre Speicherkonto erstellt, das dem Mediendienst unter Verwendung der Speicherkonto-ID-Informationen zugeordnet ist, die in der $StorageAccount Variablen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="04a00-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="04a00-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="04a00-112">PARAMETERS</span></span>

### <span data-ttu-id="04a00-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04a00-113">-DefaultProfile</span></span>
<span data-ttu-id="04a00-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="04a00-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04a00-115">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="04a00-115">-IsPrimary</span></span>
<span data-ttu-id="04a00-116">Gibt an, dass das Cmdlet das Speicherkonto als primären Speicher für den Mediendienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="04a00-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a00-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="04a00-117">-StorageAccountId</span></span>
<span data-ttu-id="04a00-118">Gibt die ID des speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="04a00-118">Specifies the ID of the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04a00-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="04a00-119">-Confirm</span></span>
<span data-ttu-id="04a00-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="04a00-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a00-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04a00-121">-WhatIf</span></span>
<span data-ttu-id="04a00-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04a00-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04a00-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="04a00-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04a00-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04a00-124">CommonParameters</span></span>
<span data-ttu-id="04a00-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04a00-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04a00-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04a00-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04a00-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="04a00-127">INPUTS</span></span>

### <span data-ttu-id="04a00-128">System. String</span><span class="sxs-lookup"><span data-stu-id="04a00-128">System.String</span></span>

## <span data-ttu-id="04a00-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="04a00-129">OUTPUTS</span></span>

### <span data-ttu-id="04a00-130">Microsoft. Azure. Commands. Media. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="04a00-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="04a00-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="04a00-131">NOTES</span></span>

## <span data-ttu-id="04a00-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="04a00-132">RELATED LINKS</span></span>

[<span data-ttu-id="04a00-133">Synchronisieren-AzMediaServiceStorageKeys</span><span class="sxs-lookup"><span data-stu-id="04a00-133">Sync-AzMediaServiceStorageKeys</span></span>](./Sync-AzMediaServiceStorageKeys.md)


