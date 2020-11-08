---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/sync-azmediaservicestoragekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
ms.openlocfilehash: 9ac16dec6403eb17f5c0bc352b7419aeb9854fec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004729"
---
# <span data-ttu-id="20756-101">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="20756-101">Sync-AzMediaServiceStorageKey</span></span>

## <span data-ttu-id="20756-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="20756-102">SYNOPSIS</span></span>
<span data-ttu-id="20756-103">Synchronisiert speicherkontoschlüssel für ein Speicherkonto, das dem Mediendienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="20756-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="20756-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="20756-104">SYNTAX</span></span>

```
Sync-AzMediaServiceStorageKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20756-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="20756-105">DESCRIPTION</span></span>
<span data-ttu-id="20756-106">Das Cmdlet " **Sync-AzMediaServiceStorageKey** " synchronisiert speicherkontoschlüssel für ein Speicherkonto, das dem Mediendienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="20756-106">The **Sync-AzMediaServiceStorageKey** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="20756-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="20756-107">EXAMPLES</span></span>

### <span data-ttu-id="20756-108">Beispiel 1: Synchronisieren von Speicherkonto Schlüsseln für ein Speicherkonto, das dem Mediendienst zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="20756-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzMediaServiceStorageKey -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="20756-109">Der erste Befehl verwendet das Get-AzStorageAccount-Cmdlet zum Abrufen des speicherkontos mit dem Namen Storage135, das zu ResourceGroup001 gehört, und speichert das Ergebnis in der Variablen mit dem Namen $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="20756-109">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="20756-110">Der zweite Befehl synchronisiert die speicherkontoschlüssel für den Mediendienst mit dem Namen MediaService001 mithilfe der **ID** -Eigenschaft, die in der $StorageAccount-Variablen enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="20756-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="20756-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="20756-111">PARAMETERS</span></span>

### <span data-ttu-id="20756-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="20756-112">-AccountName</span></span>
<span data-ttu-id="20756-113">Gibt den Namen des Medien Diensts an, den dieses Cmdlet synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="20756-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20756-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20756-114">-DefaultProfile</span></span>
<span data-ttu-id="20756-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="20756-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20756-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20756-116">-ResourceGroupName</span></span>
<span data-ttu-id="20756-117">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="20756-117">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="20756-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="20756-118">-StorageAccountId</span></span>
<span data-ttu-id="20756-119">Gibt die dem Mediendienst Konto zugeordnete Speicherkonto-ID an.</span><span class="sxs-lookup"><span data-stu-id="20756-119">Specifies the storage account ID associated with the media service account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20756-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="20756-120">-Confirm</span></span>
<span data-ttu-id="20756-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="20756-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20756-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20756-122">-WhatIf</span></span>
<span data-ttu-id="20756-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="20756-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20756-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="20756-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20756-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20756-125">CommonParameters</span></span>
<span data-ttu-id="20756-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20756-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20756-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20756-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20756-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="20756-128">INPUTS</span></span>

### <span data-ttu-id="20756-129">System. String</span><span class="sxs-lookup"><span data-stu-id="20756-129">System.String</span></span>

## <span data-ttu-id="20756-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="20756-130">OUTPUTS</span></span>

### <span data-ttu-id="20756-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="20756-131">System.Boolean</span></span>

## <span data-ttu-id="20756-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="20756-132">NOTES</span></span>

## <span data-ttu-id="20756-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="20756-133">RELATED LINKS</span></span>
