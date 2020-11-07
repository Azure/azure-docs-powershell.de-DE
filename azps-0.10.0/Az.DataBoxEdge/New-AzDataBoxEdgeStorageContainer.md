---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 8d8057953c6a5fcccd5ea561eda36c623b3e5c85
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844075"
---
# <span data-ttu-id="9da6c-101">New-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9da6c-101">New-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="9da6c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9da6c-102">SYNOPSIS</span></span>
<span data-ttu-id="9da6c-103">Erstellt einen neuen Speichercontainer im edgespeicher-Konto auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="9da6c-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="9da6c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9da6c-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9da6c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9da6c-105">DESCRIPTION</span></span>
<span data-ttu-id="9da6c-106">Das Cmdlet **New-AzDataBoxEdgeStorageContainer** erstellt einen neuen Speichercontainer im edgespeicher-Konto auf einem Daten Feld-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="9da6c-106">The **New-AzDataBoxEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Data Box Edge device.</span></span>

## <span data-ttu-id="9da6c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9da6c-107">EXAMPLES</span></span>

### <span data-ttu-id="9da6c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9da6c-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="9da6c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9da6c-109">PARAMETERS</span></span>

### <span data-ttu-id="9da6c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9da6c-110">-AsJob</span></span>
<span data-ttu-id="9da6c-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9da6c-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9da6c-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="9da6c-112">-DataFormat</span></span>
<span data-ttu-id="9da6c-113">Daten Format setzen Ex: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="9da6c-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9da6c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9da6c-114">-DefaultProfile</span></span>
<span data-ttu-id="9da6c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9da6c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9da6c-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9da6c-116">-DeviceName</span></span>
<span data-ttu-id="9da6c-117">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="9da6c-117">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9da6c-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9da6c-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="9da6c-119">Angeben des vorhandenen EdgeStorageAccount-namens</span><span class="sxs-lookup"><span data-stu-id="9da6c-119">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9da6c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9da6c-120">-Name</span></span>
<span data-ttu-id="9da6c-121">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="9da6c-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9da6c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9da6c-122">-ResourceGroupName</span></span>
<span data-ttu-id="9da6c-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="9da6c-123">Resource Group Name</span></span>

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

### <span data-ttu-id="9da6c-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9da6c-124">-Confirm</span></span>
<span data-ttu-id="9da6c-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9da6c-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9da6c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9da6c-126">-WhatIf</span></span>
<span data-ttu-id="9da6c-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9da6c-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9da6c-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9da6c-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9da6c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9da6c-129">CommonParameters</span></span>
<span data-ttu-id="9da6c-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9da6c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9da6c-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9da6c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9da6c-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9da6c-132">INPUTS</span></span>

### <span data-ttu-id="9da6c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="9da6c-133">System.String</span></span>

## <span data-ttu-id="9da6c-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9da6c-134">OUTPUTS</span></span>

### <span data-ttu-id="9da6c-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9da6c-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="9da6c-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="9da6c-136">NOTES</span></span>

## <span data-ttu-id="9da6c-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9da6c-137">RELATED LINKS</span></span>
