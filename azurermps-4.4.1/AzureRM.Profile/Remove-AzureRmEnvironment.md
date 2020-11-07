---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
ms.openlocfilehash: d27a05e652cbcd11d35536ebff97f04b3c60f520
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665008"
---
# <span data-ttu-id="34caa-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="34caa-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="34caa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="34caa-102">SYNOPSIS</span></span>
<span data-ttu-id="34caa-103">Entfernt Endpunkte und Metadaten zum Herstellen einer Verbindung mit einer bestimmten Azure-Instanz.</span><span class="sxs-lookup"><span data-stu-id="34caa-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34caa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="34caa-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34caa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34caa-105">DESCRIPTION</span></span>
<span data-ttu-id="34caa-106">Das Remove-AzureRmEnvironment-Cmdlet entfernt Endpunkte und Metadateninformationen zum Herstellen einer Verbindung mit einer bestimmten Azure-Instanz.</span><span class="sxs-lookup"><span data-stu-id="34caa-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="34caa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="34caa-107">EXAMPLES</span></span>

### <span data-ttu-id="34caa-108">Beispiel 1: Erstellen und Entfernen einer Testumgebung</span><span class="sxs-lookup"><span data-stu-id="34caa-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="34caa-109">In diesem Beispiel wird gezeigt, wie Sie mithilfe von Add-AzureRmEnvironment eine Umgebung erstellen und dann die Umgebung mithilfe von Remove-AzureRmEnvironment löschen.</span><span class="sxs-lookup"><span data-stu-id="34caa-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="34caa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="34caa-110">PARAMETERS</span></span>

### <span data-ttu-id="34caa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34caa-111">-DefaultProfile</span></span>
<span data-ttu-id="34caa-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements.</span><span class="sxs-lookup"><span data-stu-id="34caa-112">The credentials, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34caa-113">-Name</span><span class="sxs-lookup"><span data-stu-id="34caa-113">-Name</span></span>
<span data-ttu-id="34caa-114">Gibt den Namen der zu entfernenden Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="34caa-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="34caa-115">-Scope</span><span class="sxs-lookup"><span data-stu-id="34caa-115">-Scope</span></span>
<span data-ttu-id="34caa-116">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="34caa-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34caa-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="34caa-117">-Confirm</span></span>
<span data-ttu-id="34caa-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="34caa-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34caa-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34caa-119">-WhatIf</span></span>
<span data-ttu-id="34caa-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34caa-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="34caa-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="34caa-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34caa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34caa-122">CommonParameters</span></span>
<span data-ttu-id="34caa-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="34caa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34caa-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34caa-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34caa-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="34caa-125">INPUTS</span></span>

## <span data-ttu-id="34caa-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="34caa-126">OUTPUTS</span></span>

### <span data-ttu-id="34caa-127">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="34caa-127">PSAzureEnvironment</span></span>

## <span data-ttu-id="34caa-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="34caa-128">NOTES</span></span>

## <span data-ttu-id="34caa-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="34caa-129">RELATED LINKS</span></span>

[<span data-ttu-id="34caa-130">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="34caa-130">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="34caa-131">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="34caa-131">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="34caa-132">Satz-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="34caa-132">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

