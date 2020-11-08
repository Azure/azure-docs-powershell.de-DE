---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: d2821c2ab12c697c4f34ab0f5ac4bd645ccec3c7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173646"
---
# <span data-ttu-id="f84db-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="f84db-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="f84db-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f84db-102">SYNOPSIS</span></span>
<span data-ttu-id="f84db-103">Ruft die Access-Restiction-Konfiguration für eine Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="f84db-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="f84db-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f84db-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f84db-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f84db-105">DESCRIPTION</span></span>
<span data-ttu-id="f84db-106">Das Cmdlet " **Get-AzWebAppAccessRestrictionConfig** " Ruft eine Zugriffs Beschränkungs Konfiguration für eine Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="f84db-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="f84db-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f84db-107">EXAMPLES</span></span>

### <span data-ttu-id="f84db-108">Beispiel 1: Abrufen einer Web App-Zugriffs Einschränkungs Konfiguration aus einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f84db-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="f84db-109">Dieser Befehl ruft die Zugriffs Beschränkungs Konfiguration einer Web-App mit dem Namen ContosoSite ab, die zur Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="f84db-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="f84db-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f84db-110">PARAMETERS</span></span>

### <span data-ttu-id="f84db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f84db-111">-DefaultProfile</span></span>
<span data-ttu-id="f84db-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f84db-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f84db-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f84db-113">-Name</span></span>
<span data-ttu-id="f84db-114">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="f84db-114">WebApp Name</span></span>

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

### <span data-ttu-id="f84db-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f84db-115">-ResourceGroupName</span></span>
<span data-ttu-id="f84db-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="f84db-116">Resource Group Name</span></span>

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

### <span data-ttu-id="f84db-117">-Slotname</span><span class="sxs-lookup"><span data-stu-id="f84db-117">-SlotName</span></span>
<span data-ttu-id="f84db-118">Name des Bereitstellungs Steckplatzes.</span><span class="sxs-lookup"><span data-stu-id="f84db-118">Deployment Slot name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f84db-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f84db-119">CommonParameters</span></span>
<span data-ttu-id="f84db-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f84db-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f84db-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f84db-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f84db-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f84db-122">INPUTS</span></span>

### <span data-ttu-id="f84db-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f84db-123">System.String</span></span>

## <span data-ttu-id="f84db-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f84db-124">OUTPUTS</span></span>

### <span data-ttu-id="f84db-125">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="f84db-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="f84db-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="f84db-126">NOTES</span></span>

## <span data-ttu-id="f84db-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f84db-127">RELATED LINKS</span></span>

[<span data-ttu-id="f84db-128">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="f84db-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="f84db-129">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="f84db-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="f84db-130">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="f84db-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
