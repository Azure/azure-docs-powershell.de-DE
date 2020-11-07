---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8d9c783d6fe4047aa1d179cd661c88d13e9c716b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661956"
---
# <span data-ttu-id="ee9ee-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="ee9ee-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="ee9ee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ee9ee-102">SYNOPSIS</span></span>
<span data-ttu-id="ee9ee-103">Entfernt Endpunkte und Metadaten zum Herstellen einer Verbindung mit einer bestimmten Azure-Instanz.</span><span class="sxs-lookup"><span data-stu-id="ee9ee-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="ee9ee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee9ee-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee9ee-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee9ee-105">DESCRIPTION</span></span>
<span data-ttu-id="ee9ee-106">Das Remove-AzureRmEnvironment-Cmdlet entfernt Endpunkte und Metadateninformationen zum Herstellen einer Verbindung mit einer bestimmten Azure-Instanz.</span><span class="sxs-lookup"><span data-stu-id="ee9ee-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="ee9ee-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ee9ee-107">EXAMPLES</span></span>

### <span data-ttu-id="ee9ee-108">Beispiel 1: Erstellen und Entfernen einer Testumgebung</span><span class="sxs-lookup"><span data-stu-id="ee9ee-108">Example 1: Creating and removing a test environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :

PS C:\> Remove-AzureRmEnvironment -Name TestEnvironment

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
```

<span data-ttu-id="ee9ee-109">In diesem Beispiel wird gezeigt, wie Sie mithilfe von Add-AzureRmEnvironment eine Umgebung erstellen und dann die Umgebung mithilfe von Remove-AzureRmEnvironment löschen.</span><span class="sxs-lookup"><span data-stu-id="ee9ee-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="ee9ee-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee9ee-110">PARAMETERS</span></span>

### <span data-ttu-id="ee9ee-111">-Name</span><span class="sxs-lookup"><span data-stu-id="ee9ee-111">-Name</span></span>
<span data-ttu-id="ee9ee-112">Gibt den Namen der zu entfernenden Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="ee9ee-112">Specifies the name of the environment to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee9ee-113">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ee9ee-113">-Confirm</span></span>
<span data-ttu-id="ee9ee-114">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ee9ee-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee9ee-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee9ee-115">-WhatIf</span></span>
<span data-ttu-id="ee9ee-116">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ee9ee-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee9ee-117">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ee9ee-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee9ee-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee9ee-118">CommonParameters</span></span>
<span data-ttu-id="ee9ee-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee9ee-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee9ee-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee9ee-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee9ee-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ee9ee-121">INPUTS</span></span>

## <span data-ttu-id="ee9ee-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ee9ee-122">OUTPUTS</span></span>

### <span data-ttu-id="ee9ee-123">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="ee9ee-123">PSAzureEnvironment</span></span>

## <span data-ttu-id="ee9ee-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="ee9ee-124">NOTES</span></span>

## <span data-ttu-id="ee9ee-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ee9ee-125">RELATED LINKS</span></span>

[<span data-ttu-id="ee9ee-126">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="ee9ee-126">Add-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="ee9ee-127">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="ee9ee-127">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="ee9ee-128">Satz-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="ee9ee-128">Set-AzureRMEnvironment</span></span>]()

