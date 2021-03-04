---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/set-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: 7294d5c48bd8cbc94ac127ac1f1543827dc2937b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941219"
---
# <span data-ttu-id="2eca3-101">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="2eca3-101">Set-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="2eca3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2eca3-102">SYNOPSIS</span></span>
<span data-ttu-id="2eca3-103">Ändert die Oktalberechtigung einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2eca3-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2eca3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2eca3-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Permission] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2eca3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2eca3-105">DESCRIPTION</span></span>
<span data-ttu-id="2eca3-106">Das **Cmdlet Set-AzDataLakeStoreItemPermission** ändert das Berechtigungs oktal einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="2eca3-106">The **Set-AzDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="2eca3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2eca3-107">EXAMPLES</span></span>

### <span data-ttu-id="2eca3-108">Beispiel 1: Festlegen der Oktalberechtigung für ein Element</span><span class="sxs-lookup"><span data-stu-id="2eca3-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="2eca3-109">Dieser Befehl legt die Oktalberechtigung für eine Datei auf 0770 fest, was dazu führt, dass das Sticky-Bit, das Festlegen von Lese-/Schreib-/Ausführungsberechtigungen für den Besitzer der Datei, das Festlegen von Lese-/Schreib-/Ausführungsberechtigungen für die besitzende Gruppe der Datei und das Löschen von Lese-/Schreib-/Ausführungsberechtigungen für andere personen.</span><span class="sxs-lookup"><span data-stu-id="2eca3-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="2eca3-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2eca3-110">PARAMETERS</span></span>

### <span data-ttu-id="2eca3-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="2eca3-111">-Account</span></span>
<span data-ttu-id="2eca3-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="2eca3-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2eca3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eca3-113">-DefaultProfile</span></span>
<span data-ttu-id="2eca3-114">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2eca3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2eca3-115">-Path</span><span class="sxs-lookup"><span data-stu-id="2eca3-115">-Path</span></span>
<span data-ttu-id="2eca3-116">Gibt den Data Lake Store-Pfad der Datei oder des Ordners an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="2eca3-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2eca3-117">-Permission</span><span class="sxs-lookup"><span data-stu-id="2eca3-117">-Permission</span></span>
<span data-ttu-id="2eca3-118">Die Berechtigungen, die für die Datei oder den Ordner festgelegt werden müssen, ausgedrückt als Oktal (z. B. "777')</span><span class="sxs-lookup"><span data-stu-id="2eca3-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2eca3-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2eca3-119">-Confirm</span></span>
<span data-ttu-id="2eca3-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2eca3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eca3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eca3-121">-WhatIf</span></span>
<span data-ttu-id="2eca3-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2eca3-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eca3-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2eca3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eca3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eca3-124">CommonParameters</span></span>
<span data-ttu-id="2eca3-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eca3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eca3-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eca3-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eca3-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2eca3-127">INPUTS</span></span>

### <span data-ttu-id="2eca3-128">System.String</span><span class="sxs-lookup"><span data-stu-id="2eca3-128">System.String</span></span>

### <span data-ttu-id="2eca3-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="2eca3-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="2eca3-130">System.Int32</span><span class="sxs-lookup"><span data-stu-id="2eca3-130">System.Int32</span></span>

## <span data-ttu-id="2eca3-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2eca3-131">OUTPUTS</span></span>

### <span data-ttu-id="2eca3-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2eca3-132">System.Boolean</span></span>

## <span data-ttu-id="2eca3-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2eca3-133">NOTES</span></span>
* <span data-ttu-id="2eca3-134">Alias: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="2eca3-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="2eca3-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2eca3-135">RELATED LINKS</span></span>

[<span data-ttu-id="2eca3-136">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="2eca3-136">Get-AzDataLakeStoreItemPermission</span></span>](./Get-AzDataLakeStoreItemPermission.md)


