---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 54d74b40230f67a31e023ef4933d3480bc5c2b42
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94167253"
---
# <span data-ttu-id="e729b-101">New-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e729b-101">New-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="e729b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e729b-102">SYNOPSIS</span></span>
<span data-ttu-id="e729b-103">Erstellt neue Anmeldeinformationen für ein Edge-Speicherkonto auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="e729b-103">Creates new credentials for an edge storage account on the device.</span></span>

## <span data-ttu-id="e729b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e729b-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StorageAccountType <String> -StorageAccountAccessKey <SecureString> -EncryptionKey <SecureString> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e729b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e729b-105">DESCRIPTION</span></span>
<span data-ttu-id="e729b-106">Das Cmdlet **New-AzDataBoxEdgeStorageAccountCredential** erstellt eine neue Anmeldeinformationen des Edge-speicherkontos für ein Daten Feld-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="e729b-106">The **New-AzDataBoxEdgeStorageAccountCredential** cmdlet creates a new edge storage account credential for a Data Box Edge device.</span></span>

## <span data-ttu-id="e729b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e729b-107">EXAMPLES</span></span>

### <span data-ttu-id="e729b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e729b-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName device-name -Name storage-acount-credential-name -StorageAccountName storageAccountName -StorageAccountType BlobStorage -StorageAccountAccessKey @SecureString -EncryptionKey @SecureString
Name                             StorageAccount    SslStatus  ResourceGroupName
--------------------------- ---------------------- ---------- ---------------------
storageAccountCredentalName storageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="e729b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e729b-109">PARAMETERS</span></span>

### <span data-ttu-id="e729b-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e729b-110">-AsJob</span></span>
<span data-ttu-id="e729b-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e729b-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e729b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e729b-112">-DefaultProfile</span></span>
<span data-ttu-id="e729b-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e729b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e729b-114">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e729b-114">-DeviceName</span></span>
<span data-ttu-id="e729b-115">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="e729b-115">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e729b-116">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="e729b-116">-EncryptionKey</span></span>
<span data-ttu-id="e729b-117">Verschlüsselungsschlüssel des Edge-Geräts</span><span class="sxs-lookup"><span data-stu-id="e729b-117">Encryption key of the Edge device</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e729b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="e729b-118">-Name</span></span>
<span data-ttu-id="e729b-119">Name des zu verwendenden speicherkontos</span><span class="sxs-lookup"><span data-stu-id="e729b-119">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="e729b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e729b-120">-ResourceGroupName</span></span>
<span data-ttu-id="e729b-121">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="e729b-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e729b-122">-StorageAccountAccessKey</span><span class="sxs-lookup"><span data-stu-id="e729b-122">-StorageAccountAccessKey</span></span>
<span data-ttu-id="e729b-123">Bereitstellen des Zugriffsschlüssels für das Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="e729b-123">provide storage account access key</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e729b-124">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="e729b-124">-StorageAccountType</span></span>
<span data-ttu-id="e729b-125">Möglicher Speicher Zugriffstyp GeneralPurposeStorage, BlockStorage</span><span class="sxs-lookup"><span data-stu-id="e729b-125">Possible Storage Access type GeneralPurposeStorage, BlockStorage</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e729b-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e729b-126">-Confirm</span></span>
<span data-ttu-id="e729b-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e729b-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e729b-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e729b-128">-WhatIf</span></span>
<span data-ttu-id="e729b-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e729b-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e729b-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e729b-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e729b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e729b-131">CommonParameters</span></span>
<span data-ttu-id="e729b-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e729b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e729b-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e729b-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e729b-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e729b-134">INPUTS</span></span>

### <span data-ttu-id="e729b-135">Keine</span><span class="sxs-lookup"><span data-stu-id="e729b-135">None</span></span>

## <span data-ttu-id="e729b-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e729b-136">OUTPUTS</span></span>

### <span data-ttu-id="e729b-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="e729b-137">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="e729b-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="e729b-138">NOTES</span></span>

## <span data-ttu-id="e729b-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e729b-139">RELATED LINKS</span></span>
