---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/sync-azmediaservicestoragekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
ms.openlocfilehash: e9d413a8f77422b723c2dabc57d7d68c691617d8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819048"
---
# <span data-ttu-id="47824-101">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="47824-101">Sync-AzMediaServiceStorageKey</span></span>

## <span data-ttu-id="47824-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="47824-102">SYNOPSIS</span></span>
<span data-ttu-id="47824-103">Synchronisiert speicherkontoschlüssel für ein Speicherkonto, das dem Mediendienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="47824-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="47824-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="47824-104">SYNTAX</span></span>

```
Sync-AzMediaServiceStorageKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="47824-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47824-105">DESCRIPTION</span></span>
<span data-ttu-id="47824-106">Das Cmdlet " **Sync-AzMediaServiceStorageKey** " synchronisiert speicherkontoschlüssel für ein Speicherkonto, das dem Mediendienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="47824-106">The **Sync-AzMediaServiceStorageKey** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="47824-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="47824-107">EXAMPLES</span></span>

### <span data-ttu-id="47824-108">Beispiel 1: Synchronisieren von Speicherkonto Schlüsseln für ein Speicherkonto, das dem Mediendienst zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="47824-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzMediaServiceStorageKey -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="47824-109">Der erste Befehl verwendet das Get-AzStorageAccount-Cmdlet zum Abrufen des speicherkontos mit dem Namen Storage135, das zu ResourceGroup001 gehört, und speichert das Ergebnis in der Variablen mit dem Namen $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="47824-109">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="47824-110">Der zweite Befehl synchronisiert die speicherkontoschlüssel für den Mediendienst mit dem Namen MediaService001 mithilfe der **ID** -Eigenschaft, die in der $StorageAccount-Variablen enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="47824-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="47824-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="47824-111">PARAMETERS</span></span>

### <span data-ttu-id="47824-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="47824-112">-AccountName</span></span>
<span data-ttu-id="47824-113">Gibt den Namen des Medien Diensts an, den dieses Cmdlet synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="47824-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

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

### <span data-ttu-id="47824-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47824-114">-DefaultProfile</span></span>
<span data-ttu-id="47824-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="47824-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47824-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47824-116">-ResourceGroupName</span></span>
<span data-ttu-id="47824-117">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="47824-117">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="47824-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="47824-118">-StorageAccountId</span></span>
<span data-ttu-id="47824-119">Gibt die dem Mediendienst Konto zugeordnete Speicherkonto-ID an.</span><span class="sxs-lookup"><span data-stu-id="47824-119">Specifies the storage account ID associated with the media service account.</span></span>

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

### <span data-ttu-id="47824-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="47824-120">-Confirm</span></span>
<span data-ttu-id="47824-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="47824-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47824-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47824-122">-WhatIf</span></span>
<span data-ttu-id="47824-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="47824-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47824-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="47824-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47824-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47824-125">CommonParameters</span></span>
<span data-ttu-id="47824-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47824-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47824-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47824-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47824-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="47824-128">INPUTS</span></span>

### <span data-ttu-id="47824-129">System. String</span><span class="sxs-lookup"><span data-stu-id="47824-129">System.String</span></span>

## <span data-ttu-id="47824-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="47824-130">OUTPUTS</span></span>

### <span data-ttu-id="47824-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="47824-131">System.Boolean</span></span>

## <span data-ttu-id="47824-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="47824-132">NOTES</span></span>

## <span data-ttu-id="47824-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="47824-133">RELATED LINKS</span></span>
