---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: f198db6a49e1f5165dcfcd4effd91106cc0df831
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174041"
---
# <span data-ttu-id="3c0ac-101">Get-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3c0ac-101">Get-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="3c0ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3c0ac-102">SYNOPSIS</span></span>
<span data-ttu-id="3c0ac-103">Ruft die Anmeldeinformationen des speicherkontos ab, die dem Speicherkonto auf dem Gerät entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3c0ac-103">Gets the storage account credentials corresponding to the storage account on the device.</span></span>

## <span data-ttu-id="3c0ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c0ac-104">SYNTAX</span></span>

### <span data-ttu-id="3c0ac-105">ListParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="3c0ac-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c0ac-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c0ac-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3c0ac-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c0ac-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3c0ac-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c0ac-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeStorageAccountCredential [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="3c0ac-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c0ac-109">DESCRIPTION</span></span>
<span data-ttu-id="3c0ac-110">Das Cmdlet " **Get-AzStackEdgeStorageAccountCredential** " Ruft die Anmeldeinformationen des speicherkontos für das entsprechende Speicherkonto auf dem Stack-Edge-Gerät ab.</span><span class="sxs-lookup"><span data-stu-id="3c0ac-110">The **Get-AzStackEdgeStorageAccountCredential** cmdlet gets the storage account credentials for the corresponding storage account on the Stack Edge device.</span></span> <span data-ttu-id="3c0ac-111">Sie können Name, Ressourcengruppenname und Gerätenamen Parameter angeben, um Informationen zu bestimmten Speicherkonto Anmeldeinformationen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3c0ac-111">You can specify Name, Resource Group Name and Device Name parameters to get information about a specific storage account credential.</span></span>

## <span data-ttu-id="3c0ac-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3c0ac-112">EXAMPLES</span></span>

### <span data-ttu-id="3c0ac-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3c0ac-113">Example 1</span></span>
```powershell
PS C:\>  Get-AzStackEdgeStorageAccountCredential -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                          StorageAccount          SslStatus  ResourceGroupName
----------------------------- ---------------------- ---------- ---------------------
storageAccountCredentialName  StorageAccountName     Enabled    resourceGroupName
```

## <span data-ttu-id="3c0ac-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c0ac-114">PARAMETERS</span></span>

### <span data-ttu-id="3c0ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c0ac-115">-DefaultProfile</span></span>
<span data-ttu-id="3c0ac-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3c0ac-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c0ac-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3c0ac-117">-DeviceName</span></span>
<span data-ttu-id="3c0ac-118">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="3c0ac-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c0ac-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="3c0ac-119">-DeviceObject</span></span>
<span data-ttu-id="3c0ac-120">Bitte geben Sie das entsprechende Device-Objekt an</span><span class="sxs-lookup"><span data-stu-id="3c0ac-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c0ac-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3c0ac-121">-Name</span></span>
<span data-ttu-id="3c0ac-122">Name des zu verwendenden speicherkontos</span><span class="sxs-lookup"><span data-stu-id="3c0ac-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: StorageAccountCredentialName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c0ac-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c0ac-123">-ResourceGroupName</span></span>
<span data-ttu-id="3c0ac-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="3c0ac-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c0ac-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3c0ac-125">-ResourceId</span></span>
<span data-ttu-id="3c0ac-126">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="3c0ac-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3c0ac-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c0ac-127">CommonParameters</span></span>
<span data-ttu-id="3c0ac-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c0ac-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c0ac-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3c0ac-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c0ac-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3c0ac-130">INPUTS</span></span>

### <span data-ttu-id="3c0ac-131">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="3c0ac-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="3c0ac-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3c0ac-132">OUTPUTS</span></span>

### <span data-ttu-id="3c0ac-133">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="3c0ac-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="3c0ac-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="3c0ac-134">NOTES</span></span>

## <span data-ttu-id="3c0ac-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3c0ac-135">RELATED LINKS</span></span>
