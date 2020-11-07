---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccount.md
ms.openlocfilehash: 12f77d1c2b9590ef500e1df66d36929cd359a989
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844080"
---
# <span data-ttu-id="2707f-101">New-AzDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2707f-101">New-AzDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="2707f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2707f-102">SYNOPSIS</span></span>
<span data-ttu-id="2707f-103">Erstellt ein neues Edge-Speicherkonto auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="2707f-103">Creates a new Edge Storage account in the device.</span></span>

## <span data-ttu-id="2707f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2707f-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountCredentialName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-Cloud] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2707f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2707f-105">DESCRIPTION</span></span>
<span data-ttu-id="2707f-106">Das Cmdlet **New-AzDataBoxEdgeStorageAccount** erstellt ein neues Edge-Speicherkonto in einem Daten Feld-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="2707f-106">The **New-AzDataBoxEdgeStorageAccount** cmdlet creates a new Edge Storage account in a Data Box Edge device.</span></span> <span data-ttu-id="2707f-107">Bei einem Gerät kann ein Edge-Speicherkonto höchstens nur einem Cloud-Speicherkonto zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="2707f-107">For a device, one Edge Storage account can be mapped at most to only one Cloud Storage account.</span></span>

## <span data-ttu-id="2707f-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2707f-108">EXAMPLES</span></span>

### <span data-ttu-id="2707f-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2707f-109">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount1 -StorageAccountCredentialName cloudstorageaccount1 -Cloud
Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount1 0              OK     https://edgestoragegacount1.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount1     dbEdge     resourceGroupName
```

### <span data-ttu-id="2707f-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="2707f-110">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName dbEdge -Name edgestoragegacount2 -StorageAccountCredentialName cloudstorageaccount2

Name                ContainerCount Status BlobEndpoint                                                   CloudStorageAccountName DeviceName ResourceGroupName
----                -------------- -----  ------------                                                   ----------------------- ---------- -----------------
edgestoragegacount2 0              OK     https://edgestoragegacount2.blob.dbEdge.microsoftdatabox.com/ cloudstorageaccount2     dbEdge     resourceGroupName
```

<span data-ttu-id="2707f-111">2 EdgeStorageAccounts auf dem Gerät kann nicht mehr als 1 Cloud-Speicherkonto verwenden</span><span class="sxs-lookup"><span data-stu-id="2707f-111">2 EdgeStorageAccounts on the device cannot share more than 1 Cloud Storage Account</span></span>

## <span data-ttu-id="2707f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2707f-112">PARAMETERS</span></span>

### <span data-ttu-id="2707f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2707f-113">-AsJob</span></span>
<span data-ttu-id="2707f-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="2707f-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2707f-115">-Cloud</span><span class="sxs-lookup"><span data-stu-id="2707f-115">-Cloud</span></span>
<span data-ttu-id="2707f-116">Verwendet eine CloudStorageAccount für die tierung</span><span class="sxs-lookup"><span data-stu-id="2707f-116">Will use a CloudStorageAccount for tiering</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2707f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2707f-117">-DefaultProfile</span></span>
<span data-ttu-id="2707f-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2707f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2707f-119">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="2707f-119">-DeviceName</span></span>
<span data-ttu-id="2707f-120">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="2707f-120">Device Name</span></span>

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

### <span data-ttu-id="2707f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2707f-121">-Name</span></span>
<span data-ttu-id="2707f-122">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="2707f-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2707f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2707f-123">-ResourceGroupName</span></span>
<span data-ttu-id="2707f-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="2707f-124">Resource Group Name</span></span>

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

### <span data-ttu-id="2707f-125">-StorageAccountCredentialName</span><span class="sxs-lookup"><span data-stu-id="2707f-125">-StorageAccountCredentialName</span></span>
<span data-ttu-id="2707f-126">Vorhandenen StorageAccountCredential-Ressourcennamen angeben</span><span class="sxs-lookup"><span data-stu-id="2707f-126">Provide existing StorageAccountCredential's Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2707f-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2707f-127">-Confirm</span></span>
<span data-ttu-id="2707f-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2707f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2707f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2707f-129">-WhatIf</span></span>
<span data-ttu-id="2707f-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2707f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2707f-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2707f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2707f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2707f-132">CommonParameters</span></span>
<span data-ttu-id="2707f-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2707f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2707f-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2707f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2707f-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2707f-135">INPUTS</span></span>

### <span data-ttu-id="2707f-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2707f-136">System.String</span></span>

### <span data-ttu-id="2707f-137">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="2707f-137">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2707f-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2707f-138">OUTPUTS</span></span>

### <span data-ttu-id="2707f-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2707f-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccount</span></span>

## <span data-ttu-id="2707f-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="2707f-140">NOTES</span></span>

## <span data-ttu-id="2707f-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2707f-141">RELATED LINKS</span></span>
