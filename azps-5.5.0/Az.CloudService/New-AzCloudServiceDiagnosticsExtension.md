---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/new-azcloudservicediagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/New-AzCloudServiceDiagnosticsExtension.md
ms.openlocfilehash: 96651a495f08657a4cd9006545cfa104285ec7ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167972"
---
# <span data-ttu-id="c808d-101">New-AzCloudServiceDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="c808d-101">New-AzCloudServiceDiagnosticsExtension</span></span>

## <span data-ttu-id="c808d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c808d-102">SYNOPSIS</span></span>
<span data-ttu-id="c808d-103">Erstellen eines Speicherobjekts für die Diagnoseerweiterung</span><span class="sxs-lookup"><span data-stu-id="c808d-103">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="c808d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c808d-104">SYNTAX</span></span>

```
New-AzCloudServiceDiagnosticsExtension [-Name] <String> [-ResourceGroupName] <String>
 [-CloudServiceName] <String> [-DiagnosticsConfigurationPath] <String> [-StorageAccountName] <String>
 [-StorageAccountKey] <String> [[-Subscription] <String>] [[-TypeHandlerVersion] <String>]
 [[-RolesAppliedTo] <String[]>] [[-AutoUpgradeMinorVersion] <Boolean>] [<CommonParameters>]
```

## <span data-ttu-id="c808d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c808d-105">DESCRIPTION</span></span>
<span data-ttu-id="c808d-106">Erstellen eines Speicherobjekts für die Diagnoseerweiterung</span><span class="sxs-lookup"><span data-stu-id="c808d-106">Create a in-memory object for Diagnostics Extension</span></span>

## <span data-ttu-id="c808d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c808d-107">EXAMPLES</span></span>

### <span data-ttu-id="c808d-108">Beispiel 1: Erstellen eines Diagnoseerweiterungsobjekts</span><span class="sxs-lookup"><span data-stu-id="c808d-108">Example 1: Create diagnostics extension object</span></span>
```powershell
PS C:\> $storageAccountKey = Get-AzStorageAccountKey -ResourceGroupName "ContosOrg" -Name "ContosSA"
PS C:\> $configFile = "<WAD configuration file path>"
PS C:\> $extension = New-AzCloudServiceDiagnosticsExtension -Name "WADExtension" -ResourceGroupName "ContosOrg" -CloudServiceName "ContosCS" -StorageAccountName "ContosSA" -StorageAccountKey $storageAccountKey[0].Value -DiagnosticsConfigurationPath $configFile -TypeHandlerVersion "1.5" -AutoUpgradeMinorVersion $true
```

<span data-ttu-id="c808d-109">Dieser Befehl erstellt ein Diagnoseerweiterungsobjekt, das zum Erstellen oder Aktualisieren eines Clouddiensts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c808d-109">This command creates diagnostics extension object which is used for creating or updating a cloud service.</span></span>
<span data-ttu-id="c808d-110">Weitere Details finden Sie unter "New-AzCloudService".</span><span class="sxs-lookup"><span data-stu-id="c808d-110">For more details see New-AzCloudService.</span></span>

## <span data-ttu-id="c808d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c808d-111">PARAMETERS</span></span>

### <span data-ttu-id="c808d-112">-AutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="c808d-112">-AutoUpgradeMinorVersion</span></span>
<span data-ttu-id="c808d-113">Nebenversion für automatisches Upgrade</span><span class="sxs-lookup"><span data-stu-id="c808d-113">Auto upgrade minor version.</span></span>

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

### <span data-ttu-id="c808d-114">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="c808d-114">-CloudServiceName</span></span>
<span data-ttu-id="c808d-115">Name des Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="c808d-115">Name of Cloud Service.</span></span>

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

### <span data-ttu-id="c808d-116">-DiagnosticsConfigurationPath</span><span class="sxs-lookup"><span data-stu-id="c808d-116">-DiagnosticsConfigurationPath</span></span>
<span data-ttu-id="c808d-117">Gibt die Konfiguration für die Azure Diagnostics an.</span><span class="sxs-lookup"><span data-stu-id="c808d-117">Specifies the configuration for Azure Diagnostics.</span></span>
<span data-ttu-id="c808d-118">Sie können das Schema mit dem folgenden Befehl herunterladen: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics'). PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'</span><span class="sxs-lookup"><span data-stu-id="c808d-118">You can download the schema by using the following command: (Get-AzureServiceAvailableExtension -ExtensionName 'PaaSDiagnostics' -ProviderNamespace 'Microsoft.Azure.Diagnostics').PublicConfigurationSchema | Out-File -Encoding utf8 -FilePath 'WadConfig.xsd'</span></span>

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

### <span data-ttu-id="c808d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c808d-119">-Name</span></span>
<span data-ttu-id="c808d-120">Name der Diagnoseerweiterung.</span><span class="sxs-lookup"><span data-stu-id="c808d-120">Name of Diagnostics Extension.</span></span>

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

### <span data-ttu-id="c808d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c808d-121">-ResourceGroupName</span></span>
<span data-ttu-id="c808d-122">Ressourcengruppenname des Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="c808d-122">Resource Group name of Cloud Service.</span></span>

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

### <span data-ttu-id="c808d-123">-RolesAppliedTo</span><span class="sxs-lookup"><span data-stu-id="c808d-123">-RolesAppliedTo</span></span>
<span data-ttu-id="c808d-124">Auf rollen angewendete Rollen.</span><span class="sxs-lookup"><span data-stu-id="c808d-124">Roles applied to.</span></span>

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

### <span data-ttu-id="c808d-125">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c808d-125">-StorageAccountKey</span></span>
<span data-ttu-id="c808d-126">Speicherkontoschlüssel.</span><span class="sxs-lookup"><span data-stu-id="c808d-126">Storage Account Key.</span></span>

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

### <span data-ttu-id="c808d-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c808d-127">-StorageAccountName</span></span>
<span data-ttu-id="c808d-128">Der Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="c808d-128">Name of the Storage Account.</span></span>

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

### <span data-ttu-id="c808d-129">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="c808d-129">-Subscription</span></span>
<span data-ttu-id="c808d-130">Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c808d-130">Subscription.</span></span>

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

### <span data-ttu-id="c808d-131">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="c808d-131">-TypeHandlerVersion</span></span>
<span data-ttu-id="c808d-132">Gibt die Version der Erweiterung an.</span><span class="sxs-lookup"><span data-stu-id="c808d-132">Specifies the version of the extension.</span></span>

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

### <span data-ttu-id="c808d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c808d-133">CommonParameters</span></span>
<span data-ttu-id="c808d-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c808d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c808d-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c808d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c808d-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c808d-136">INPUTS</span></span>

## <span data-ttu-id="c808d-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c808d-137">OUTPUTS</span></span>

### <span data-ttu-id="c808d-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span><span class="sxs-lookup"><span data-stu-id="c808d-138">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.Extension</span></span>

## <span data-ttu-id="c808d-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c808d-139">NOTES</span></span>

<span data-ttu-id="c808d-140">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c808d-140">ALIASES</span></span>

## <span data-ttu-id="c808d-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c808d-141">RELATED LINKS</span></span>

