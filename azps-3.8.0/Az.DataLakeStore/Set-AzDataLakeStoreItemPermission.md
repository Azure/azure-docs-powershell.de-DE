---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 6ACE045E-67AD-40FE-86E4-450AF522F174
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/set-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Set-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: af14588394a94e771c1287081aa263a7ba8e9da1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005227"
---
# <span data-ttu-id="e247d-101">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="e247d-101">Set-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="e247d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e247d-102">SYNOPSIS</span></span>
<span data-ttu-id="e247d-103">Ändert die Berechtigung Oktal einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e247d-103">Modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e247d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e247d-104">SYNTAX</span></span>

```
Set-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Permission] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e247d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e247d-105">DESCRIPTION</span></span>
<span data-ttu-id="e247d-106">Das Cmdlet " **Satz-AzDataLakeStoreItemPermission** " ändert die Berechtigung Oktal einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e247d-106">The **Set-AzDataLakeStoreItemPermission** cmdlet modifies the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="e247d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e247d-107">EXAMPLES</span></span>

### <span data-ttu-id="e247d-108">Beispiel 1: Einrichten der oktalen Berechtigung für ein Element</span><span class="sxs-lookup"><span data-stu-id="e247d-108">Example 1: Set the permission octal for an item</span></span>
```
PS C:\>Set-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt" -Permission 0770
```

<span data-ttu-id="e247d-109">Mit diesem Befehl wird die Berechtigung Oktal für eine Datei auf 0770 festgelegt, was zum Löschen des Sticky-Bits, zum Festlegen von Berechtigungen zum Lesen/Schreiben/ausführen für den Besitzer der Datei, zum Festlegen von Berechtigungen zum Lesen/Schreiben/ausführen für die besitzende Gruppe der Datei und zum Löschen von Berechtigungen zum Lesen/Schreiben/ausführen für andere Personen führt.</span><span class="sxs-lookup"><span data-stu-id="e247d-109">This command sets the permission octal for a file to 0770, which translates to clearing the sticky bit, setting read/write/execute permissions for the owner of the file, setting read/write/execute permissions for the owning group of the file, and clearing read/write/execute permissions for other.</span></span>

## <span data-ttu-id="e247d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e247d-110">PARAMETERS</span></span>

### <span data-ttu-id="e247d-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="e247d-111">-Account</span></span>
<span data-ttu-id="e247d-112">Gibt den Namen des Daten Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="e247d-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="e247d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e247d-113">-DefaultProfile</span></span>
<span data-ttu-id="e247d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e247d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e247d-115">-Path</span><span class="sxs-lookup"><span data-stu-id="e247d-115">-Path</span></span>
<span data-ttu-id="e247d-116">Gibt den Daten See-Speicherpfad der Datei oder des Ordners an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="e247d-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="e247d-117">-Berechtigung</span><span class="sxs-lookup"><span data-stu-id="e247d-117">-Permission</span></span>
<span data-ttu-id="e247d-118">Die Berechtigungen für die Datei oder den Ordner, ausgedrückt als oktal (z. b. "777")</span><span class="sxs-lookup"><span data-stu-id="e247d-118">The permissions to set for the file or folder, expressed as an octal (e.g. '777')</span></span>

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

### <span data-ttu-id="e247d-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e247d-119">-Confirm</span></span>
<span data-ttu-id="e247d-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e247d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e247d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e247d-121">-WhatIf</span></span>
<span data-ttu-id="e247d-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e247d-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e247d-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e247d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e247d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e247d-124">CommonParameters</span></span>
<span data-ttu-id="e247d-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e247d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e247d-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e247d-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e247d-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e247d-127">INPUTS</span></span>

### <span data-ttu-id="e247d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="e247d-128">System.String</span></span>

### <span data-ttu-id="e247d-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="e247d-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="e247d-130">System. Int32</span><span class="sxs-lookup"><span data-stu-id="e247d-130">System.Int32</span></span>

## <span data-ttu-id="e247d-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e247d-131">OUTPUTS</span></span>

### <span data-ttu-id="e247d-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e247d-132">System.Boolean</span></span>

## <span data-ttu-id="e247d-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="e247d-133">NOTES</span></span>
* <span data-ttu-id="e247d-134">Alias: Set-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="e247d-134">Alias: Set-AdlStoreItemPermission</span></span>

## <span data-ttu-id="e247d-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e247d-135">RELATED LINKS</span></span>

[<span data-ttu-id="e247d-136">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="e247d-136">Get-AzDataLakeStoreItemPermission</span></span>](./Get-AzDataLakeStoreItemPermission.md)


