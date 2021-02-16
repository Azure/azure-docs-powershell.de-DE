---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: F395E192-80FA-421D-A389-8C5C0C2267E4
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/sync-azmediaservicestoragekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Sync-AzMediaServiceStorageKey.md
ms.openlocfilehash: 9ac16dec6403eb17f5c0bc352b7419aeb9854fec
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161361"
---
# <span data-ttu-id="c93fc-101">Sync-AzMediaServiceStorageKey</span><span class="sxs-lookup"><span data-stu-id="c93fc-101">Sync-AzMediaServiceStorageKey</span></span>

## <span data-ttu-id="c93fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c93fc-102">SYNOPSIS</span></span>
<span data-ttu-id="c93fc-103">Synchronisiert Speicherkontoschlüssel für ein Speicherkonto, das dem Mediendienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c93fc-103">Synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="c93fc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c93fc-104">SYNTAX</span></span>

```
Sync-AzMediaServiceStorageKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-StorageAccountId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c93fc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c93fc-105">DESCRIPTION</span></span>
<span data-ttu-id="c93fc-106">Das **Cmdlet "Sync-AzMediaServiceStorageKey"** synchronisiert Speicherkontoschlüssel für ein Speicherkonto, das dem Mediendienst zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c93fc-106">The **Sync-AzMediaServiceStorageKey** cmdlet synchronizes storage account keys for a storage account associated with the media service.</span></span>

## <span data-ttu-id="c93fc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c93fc-107">EXAMPLES</span></span>

### <span data-ttu-id="c93fc-108">Beispiel 1: Synchronisieren von Speicherkontoschlüsseln für ein Speicherkonto, das dem Mediendienst zugeordnet ist</span><span class="sxs-lookup"><span data-stu-id="c93fc-108">Example 1: Synchronize storage account keys for a storage account associated with the media service</span></span>
```
PS C:\>$StorageAccount = Get-AzStorageAccount -ResourceGroupName "ResourceGroup001" -Name "Storage135"
PS C:\> Sync-AzMediaServiceStorageKey -ResourceGroupName "ResourceGroup001" -AccoutName "MediasService001" -StorageAccoutId $StorageAccount.Id
```

<span data-ttu-id="c93fc-109">Der erste Befehl verwendet das Get-AzStorageAccount-Cmdlet, um das Speicherkonto namens "Storage135" zu erhalten, das zu "ResourceGroup001" gehört, und speichert das Ergebnis in der Variablen namens $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="c93fc-109">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named Storage135 that belongs to ResourceGroup001 and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="c93fc-110">Der zweite Befehl synchronisiert die Speicherkontoschlüssel für den Mediendienst  mit dem Namen MediaService001 und verwendet dazu die ID-Eigenschaft, die in der variablen $StorageAccount ist.</span><span class="sxs-lookup"><span data-stu-id="c93fc-110">The second command synchronizes the storage account keys for the media service named MediaService001 using the **Id** property contained in the $StorageAccount variable.</span></span>

## <span data-ttu-id="c93fc-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c93fc-111">PARAMETERS</span></span>

### <span data-ttu-id="c93fc-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c93fc-112">-AccountName</span></span>
<span data-ttu-id="c93fc-113">Gibt den Namen des Mediendiensts an, der von diesem Cmdlet synchronisiert wird.</span><span class="sxs-lookup"><span data-stu-id="c93fc-113">Specifies the name of the media service that this cmdlet synchronizes.</span></span>

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

### <span data-ttu-id="c93fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c93fc-114">-DefaultProfile</span></span>
<span data-ttu-id="c93fc-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c93fc-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c93fc-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c93fc-116">-ResourceGroupName</span></span>
<span data-ttu-id="c93fc-117">Gibt den Namen der Ressourcengruppe an, die den Mediendienst enthält.</span><span class="sxs-lookup"><span data-stu-id="c93fc-117">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="c93fc-118">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="c93fc-118">-StorageAccountId</span></span>
<span data-ttu-id="c93fc-119">Gibt die Speicherkonto-ID an, die dem Mediendienstkonto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c93fc-119">Specifies the storage account ID associated with the media service account.</span></span>

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

### <span data-ttu-id="c93fc-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c93fc-120">-Confirm</span></span>
<span data-ttu-id="c93fc-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c93fc-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c93fc-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c93fc-122">-WhatIf</span></span>
<span data-ttu-id="c93fc-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c93fc-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c93fc-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c93fc-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c93fc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c93fc-125">CommonParameters</span></span>
<span data-ttu-id="c93fc-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c93fc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c93fc-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c93fc-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c93fc-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c93fc-128">INPUTS</span></span>

### <span data-ttu-id="c93fc-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c93fc-129">System.String</span></span>

## <span data-ttu-id="c93fc-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c93fc-130">OUTPUTS</span></span>

### <span data-ttu-id="c93fc-131">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c93fc-131">System.Boolean</span></span>

## <span data-ttu-id="c93fc-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c93fc-132">NOTES</span></span>

## <span data-ttu-id="c93fc-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c93fc-133">RELATED LINKS</span></span>
