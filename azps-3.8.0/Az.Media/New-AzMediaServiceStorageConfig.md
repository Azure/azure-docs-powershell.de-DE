---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 4D64CA4D-1066-4D3E-9317-60D37D9DE2BB
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/new-azmediaservicestorageconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/New-AzMediaServiceStorageConfig.md
ms.openlocfilehash: 4f929c720859df529dbf2954da9ddb51eedec8b4
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409289"
---
# <span data-ttu-id="4460c-101">New-AzMediaServiceStorageConfig</span><span class="sxs-lookup"><span data-stu-id="4460c-101">New-AzMediaServiceStorageConfig</span></span>

## <span data-ttu-id="4460c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4460c-102">SYNOPSIS</span></span>
<span data-ttu-id="4460c-103">Erstellen Sie eine Speicherkontokonfiguration für die Mediendienst-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4460c-103">Create a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="4460c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4460c-104">SYNTAX</span></span>

```
New-AzMediaServiceStorageConfig [-DefaultProfile <IAzureContextContainer>] [-StorageAccountId] <String>
 [-IsPrimary] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4460c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4460c-105">DESCRIPTION</span></span>
<span data-ttu-id="4460c-106">Das **Cmdlet "New-AzMediaServiceStorageConfig"** erstellt eine Speicherkontokonfiguration für die Mediendienst-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="4460c-106">The **New-AzMediaServiceStorageConfig** cmdlet creates a storage account configuration for the media service cmdlets.</span></span>

## <span data-ttu-id="4460c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4460c-107">EXAMPLES</span></span>

### <span data-ttu-id="4460c-108">Beispiel 1: Erstellen einer Speicherkontokonfiguration für die Mediendienst-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="4460c-108">Example 1: Create a storage account configuration for the media service cmdlets</span></span>
```
PS C:\>
$StorageAccount = New-AzStorageAccount -ResourceGroupName $ResourceGroupName -Name "Storage1" -Location "East US" -Type "Standard_GRS"

PS C:\> New-AzMediaServiceStorageConfig -StorageAccountId $StorageAccount.Id -IsPrimary
```

<span data-ttu-id="4460c-109">Der erste Befehl erstellt mithilfe des **Cmdlets "New-AzStorageAccount"** ein Speicherkontoobjekt.</span><span class="sxs-lookup"><span data-stu-id="4460c-109">The first command creates a storage account object by using **the New-AzStorageAccount** cmdlet.</span></span>
<span data-ttu-id="4460c-110">Der Befehl nennt dieses Speicherkonto "Storage1" und der Typ "Standard_GRS und speichert das Ergebnis in der Variablen namens $StorageAccount.</span><span class="sxs-lookup"><span data-stu-id="4460c-110">The command names this storage account Storage1 and the type is named Standard_GRS and stores the result in the variable named $StorageAccount.</span></span>
<span data-ttu-id="4460c-111">Der zweite Befehl erstellt ein Speicherkonfigurationsobjekt als primäres Speicherkonto, das dem Mediendienst zugeordnet ist, und verwendet dazu die in der Variablen $StorageAccount Speicherkonto-ID.</span><span class="sxs-lookup"><span data-stu-id="4460c-111">The second command creates a storage configuration object as the primary storage account associated with the media service using the storage account ID information stored in the $StorageAccount variable.</span></span>

## <span data-ttu-id="4460c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4460c-112">PARAMETERS</span></span>

### <span data-ttu-id="4460c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4460c-113">-DefaultProfile</span></span>
<span data-ttu-id="4460c-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4460c-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4460c-115">-IsPrimary</span><span class="sxs-lookup"><span data-stu-id="4460c-115">-IsPrimary</span></span>
<span data-ttu-id="4460c-116">Gibt an, dass das Cmdlet das Speicherkonto als primären Speicher für den Mediendienst erstellt.</span><span class="sxs-lookup"><span data-stu-id="4460c-116">Indicates that the cmdlet creates the storage account as the primary storage for the media service.</span></span>

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

### <span data-ttu-id="4460c-117">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="4460c-117">-StorageAccountId</span></span>
<span data-ttu-id="4460c-118">Gibt die ID des Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="4460c-118">Specifies the ID of the storage account.</span></span>

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

### <span data-ttu-id="4460c-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4460c-119">-Confirm</span></span>
<span data-ttu-id="4460c-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4460c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4460c-121">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4460c-121">-WhatIf</span></span>
<span data-ttu-id="4460c-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4460c-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4460c-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4460c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4460c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4460c-124">CommonParameters</span></span>
<span data-ttu-id="4460c-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4460c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4460c-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4460c-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4460c-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4460c-127">INPUTS</span></span>

### <span data-ttu-id="4460c-128">System.String</span><span class="sxs-lookup"><span data-stu-id="4460c-128">System.String</span></span>

## <span data-ttu-id="4460c-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4460c-129">OUTPUTS</span></span>

### <span data-ttu-id="4460c-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4460c-130">Microsoft.Azure.Commands.Media.Models.PSStorageAccount</span></span>

## <span data-ttu-id="4460c-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4460c-131">NOTES</span></span>

## <span data-ttu-id="4460c-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4460c-132">RELATED LINKS</span></span>



