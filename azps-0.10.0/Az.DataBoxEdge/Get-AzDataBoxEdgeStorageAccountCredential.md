---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeStorageAccountCredential.md
ms.openlocfilehash: 4bc1e887ba1f5fc9918c6b01858cf9bd2c116ca6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844123"
---
# <span data-ttu-id="af9b3-101">Get-AzDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="af9b3-101">Get-AzDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="af9b3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="af9b3-102">SYNOPSIS</span></span>
<span data-ttu-id="af9b3-103">Ruft die Anmeldeinformationen des speicherkontos ab, die dem Speicherkonto auf dem Gerät entsprechen.</span><span class="sxs-lookup"><span data-stu-id="af9b3-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="af9b3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="af9b3-104">SYNTAX</span></span>

### <span data-ttu-id="af9b3-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="af9b3-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af9b3-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="af9b3-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="af9b3-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="af9b3-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="af9b3-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="af9b3-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="af9b3-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="af9b3-109">DESCRIPTION</span></span>
<span data-ttu-id="af9b3-110">Das Cmdlet " **Get-AzDataBoxEdgeStorageAccountCredential** " Ruft die Anmeldeinformationen des speicherkontos für das entsprechende Speicherkonto auf dem Daten Feld-Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="af9b3-110">The **Get-AzDataBoxEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Data Box Edge device.</span></span> <span data-ttu-id="af9b3-111">Sie können Name, Ressourcengruppenname und Gerätenamen Parameter angeben, um Informationen zu bestimmten Speicherkonto Anmeldeinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="af9b3-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="af9b3-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="af9b3-112">EXAMPLES</span></span>

### <span data-ttu-id="af9b3-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="af9b3-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzDataBoxEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="af9b3-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="af9b3-114">PARAMETERS</span></span>

### <span data-ttu-id="af9b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af9b3-115">-DefaultProfile</span></span>
<span data-ttu-id="af9b3-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="af9b3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af9b3-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="af9b3-117">-DeviceName</span></span>
<span data-ttu-id="af9b3-118">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="af9b3-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af9b3-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="af9b3-119">-DeviceObject</span></span>
<span data-ttu-id="af9b3-120">Bitte geben Sie das entsprechende Device-Objekt an</span><span class="sxs-lookup"><span data-stu-id="af9b3-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="af9b3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="af9b3-121">-Name</span></span>
<span data-ttu-id="af9b3-122">Name des zu verwendenden speicherkontos</span><span class="sxs-lookup"><span data-stu-id="af9b3-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af9b3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af9b3-123">-ResourceGroupName</span></span>
<span data-ttu-id="af9b3-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="af9b3-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af9b3-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="af9b3-125">-ResourceId</span></span>
<span data-ttu-id="af9b3-126">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="af9b3-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af9b3-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af9b3-127">CommonParameters</span></span>
<span data-ttu-id="af9b3-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af9b3-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af9b3-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af9b3-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af9b3-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="af9b3-130">INPUTS</span></span>

### <span data-ttu-id="af9b3-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="af9b3-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="af9b3-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="af9b3-132">OUTPUTS</span></span>

### <span data-ttu-id="af9b3-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="af9b3-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="af9b3-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="af9b3-134">NOTES</span></span>

## <span data-ttu-id="af9b3-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="af9b3-135">RELATED LINKS</span></span>
