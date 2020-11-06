---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Remove-AzureRmEnvironment.md
ms.openlocfilehash: 2916a4048987d703bc1cbb44653eae2cfb066a29
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502526"
---
# <span data-ttu-id="96352-101">Remove-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="96352-101">Remove-AzureRmEnvironment</span></span>

## <span data-ttu-id="96352-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96352-102">SYNOPSIS</span></span>
<span data-ttu-id="96352-103">Entfernt Endpunkte und Metadaten zum Herstellen einer Verbindung mit einer bestimmten Azure-Instanz.</span><span class="sxs-lookup"><span data-stu-id="96352-103">Removes endpoints and metadata for connecting to a given Azure instance.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="96352-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96352-104">SYNTAX</span></span>

```
Remove-AzureRmEnvironment [-Name] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96352-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96352-105">DESCRIPTION</span></span>
<span data-ttu-id="96352-106">Das Remove-AzureRmEnvironment-Cmdlet entfernt Endpunkte und Metadateninformationen zum Herstellen einer Verbindung mit einer bestimmten Azure-Instanz.</span><span class="sxs-lookup"><span data-stu-id="96352-106">The Remove-AzureRmEnvironment cmdlet removes endpoints and metadata information for connecting to a given Azure instance.</span></span>

## <span data-ttu-id="96352-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96352-107">EXAMPLES</span></span>

### <span data-ttu-id="96352-108">Beispiel 1: Erstellen und Entfernen einer Testumgebung</span><span class="sxs-lookup"><span data-stu-id="96352-108">Example 1: Creating and removing a test environment</span></span>
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

<span data-ttu-id="96352-109">In diesem Beispiel wird gezeigt, wie Sie mithilfe von Add-AzureRmEnvironment eine Umgebung erstellen und dann die Umgebung mithilfe von Remove-AzureRmEnvironment löschen.</span><span class="sxs-lookup"><span data-stu-id="96352-109">This example shows how to create an environment using Add-AzureRmEnvironment, and then how to delete the environment using Remove-AzureRmEnvironment.</span></span>

## <span data-ttu-id="96352-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="96352-110">PARAMETERS</span></span>

### <span data-ttu-id="96352-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96352-111">-DefaultProfile</span></span>
<span data-ttu-id="96352-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements.</span><span class="sxs-lookup"><span data-stu-id="96352-112">The credentials, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96352-113">-Name</span><span class="sxs-lookup"><span data-stu-id="96352-113">-Name</span></span>
<span data-ttu-id="96352-114">Gibt den Namen der zu entfernenden Umgebung an.</span><span class="sxs-lookup"><span data-stu-id="96352-114">Specifies the name of the environment to remove.</span></span>

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

### <span data-ttu-id="96352-115">-Scope</span><span class="sxs-lookup"><span data-stu-id="96352-115">-Scope</span></span>
<span data-ttu-id="96352-116">Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.</span><span class="sxs-lookup"><span data-stu-id="96352-116">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96352-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="96352-117">-Confirm</span></span>
<span data-ttu-id="96352-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="96352-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96352-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96352-119">-WhatIf</span></span>
<span data-ttu-id="96352-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="96352-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96352-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96352-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96352-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96352-122">CommonParameters</span></span>
<span data-ttu-id="96352-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96352-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96352-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96352-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96352-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96352-125">INPUTS</span></span>

### <span data-ttu-id="96352-126">Keine</span><span class="sxs-lookup"><span data-stu-id="96352-126">None</span></span>
<span data-ttu-id="96352-127">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="96352-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="96352-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96352-128">OUTPUTS</span></span>

### <span data-ttu-id="96352-129">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="96352-129">PSAzureEnvironment</span></span>

## <span data-ttu-id="96352-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="96352-130">NOTES</span></span>

## <span data-ttu-id="96352-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96352-131">RELATED LINKS</span></span>

[<span data-ttu-id="96352-132">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="96352-132">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="96352-133">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="96352-133">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="96352-134">Satz-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="96352-134">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

