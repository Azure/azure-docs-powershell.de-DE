---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/powershell/module/az.cloudservice/new-azcloudservicediagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
ms.openlocfilehash: a87e9c76b2c083392fc37d74a3ba213dba5881ee
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927419"
---
# <span data-ttu-id="6b644-101">New-AzCloudServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="6b644-101">New-AzCloudServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="6b644-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b644-102">SYNOPSIS</span></span>
<span data-ttu-id="6b644-103">Erstellen eines Speicherobjekts für die Diagnoseerweiterung</span><span class="sxs-lookup"><span data-stu-id="6b644-103">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="6b644-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b644-104">SYNTAX</span></span>

```
New-AzCloudServiceDiagnosticsExtension [-Name] <String> [-ResourceGroupName] <String>
 [-CloudServiceName] <String> [-DiagnosticsConfigurationPath] <String> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [[-Subscription] <String>] [[-TypeHandlerVersion] <String>]
 [[-RolesAppliedTo] <String[]>] [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="6b644-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b644-105">DESCRIPTION</span></span>
<span data-ttu-id="6b644-106">Erstellen eines Speicherobjekts für die Diagnoseerweiterung</span><span class="sxs-lookup"><span data-stu-id="6b644-106">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="6b644-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6b644-107">EXAMPLES</span></span>

### <span data-ttu-id="6b644-108">Beispiel 1: Erstellen eines Diagnoseerweiterungsobjekts</span><span class="sxs-lookup"><span data-stu-id="6b644-108">Example 1: Create diagnostics extension object</span></span>
```powershell
PS C:\> $storageAccountKey = Get-AzStorageAccountKey -ResourceGroupName "ContosOrg" -Name "ContosSA"
PS C:\> $configFile = "<WAD configuration file path>"
PS C:\> $extension = New-AzCloudServiceDiagnosticsExtension -Name "WADExtension" -ResourceGroupName "ContosOrg" -CloudServiceName "ContosCS" -StorageAccountName "ContosSA" -StorageAccountKey $storageAccountKey[0].Value -DiagnosticsConfigurationPath $configFile -TypeHandlerVersion "1.5" -AutoUpgradeMinorVersion $true
```

<span data-ttu-id="6b644-109">Mit diesem Befehl wird ein Diagnoseerweiterungsobjekt erstellt, das zum Erstellen oder Aktualisieren eines Clouddiensts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6b644-109">This command creates diagnostics extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="6b644-110">Weitere Informationen finden Sie unter New-AzCloudService.</span><span class="sxs-lookup"><span data-stu-id="6b644-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="6b644-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6b644-111">PARAMETERS</span></span>

### <span data-ttu-id="6b644-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="6b644-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="6b644-113">Nebenversion für automatisches Upgrade.</span><span class="sxs-lookup"><span data-stu-id="6b644-113">Auto upgrade minor version.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b644-114">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="6b644-114">-CloudServiceName</span></span>
<span data-ttu-id="6b644-115">Name des Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="6b644-115">Name of Cloud Service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b644-116">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="6b644-116">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="6b644-117">Gibt die Konfiguration für Azure Diagnostics an.</span><span class="sxs-lookup"><span data-stu-id="6b644-117">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="6b644-118">Sie können das Schema mit dem folgenden Befehl herunterladen: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics'). PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'</span><span class="sxs-lookup"><span data-stu-id="6b644-118">You can download the schema by using the following command: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b644-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6b644-119">-Name</span></span>
<span data-ttu-id="6b644-120">Name der Diagnoseerweiterung.</span><span class="sxs-lookup"><span data-stu-id="6b644-120">Name of Diagnostics Extension.</span></span>

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

### <span data-ttu-id="6b644-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b644-121">-ResourceGroupName</span></span>
<span data-ttu-id="6b644-122">Name der Ressourcengruppe des Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="6b644-122">Resource Group name of Cloud Service.</span></span>

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

### <span data-ttu-id="6b644-123">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="6b644-123">-RolesAppliedTo</span></span>
<span data-ttu-id="6b644-124">Auf angewendete Rollen.</span><span class="sxs-lookup"><span data-stu-id="6b644-124">Roles applied to.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b644-125">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6b644-125">-StorageAccountKey</span></span>
<span data-ttu-id="6b644-126">Speicherkontoschlüssel.</span><span class="sxs-lookup"><span data-stu-id="6b644-126">Storage Account Key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b644-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6b644-127">-StorageAccountName</span></span>
<span data-ttu-id="6b644-128">Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="6b644-128">Name of the Storage Account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b644-129">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="6b644-129">-Subscription</span></span>
<span data-ttu-id="6b644-130">Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6b644-130">Subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b644-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="6b644-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="6b644-132">Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="6b644-132">Specifies the version of the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b644-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b644-133">CommonParameters</span></span>
<span data-ttu-id="6b644-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b644-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b644-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b644-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b644-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6b644-136">INPUTS</span></span>

## <span data-ttu-id="6b644-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6b644-137">OUTPUTS</span></span>

### <span data-ttu-id="6b644-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="6b644-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="6b644-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6b644-139">NOTES</span></span>

<span data-ttu-id="6b644-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="6b644-140">ALIASES</span></span>

## <span data-ttu-id="6b644-141">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6b644-141">RELATED LINKS</span></span>

