---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppAccessRestrictionConfig.md
ms.openlocfilehash: d2821c2ab12c697c4f34ab0f5ac4bd645ccec3c7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175942"
---
# <span data-ttu-id="370e5-101">Get-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="370e5-101">Get-AzWebAppAccessRestrictionConfig</span></span>

## <span data-ttu-id="370e5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="370e5-102">SYNOPSIS</span></span>
<span data-ttu-id="370e5-103">Ruft die Access-Restiction-Konfiguration für eine Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="370e5-103">Gets Access Restiction configuration for an Azure Web App.</span></span>

## <span data-ttu-id="370e5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="370e5-104">SYNTAX</span></span>

```
Get-AzWebAppAccessRestrictionConfig [-ResourceGroupName] <String> [-Name] <String> [[-SlotName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="370e5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="370e5-105">DESCRIPTION</span></span>
<span data-ttu-id="370e5-106">Das Cmdlet " **Get-AzWebAppAccessRestrictionConfig** " Ruft eine Zugriffs Beschränkungs Konfiguration für eine Azure Web App ab.</span><span class="sxs-lookup"><span data-stu-id="370e5-106">The **Get-AzWebAppAccessRestrictionConfig** cmdlet gets Access Restriction config about an Azure Web App.</span></span>

## <span data-ttu-id="370e5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="370e5-107">EXAMPLES</span></span>

### <span data-ttu-id="370e5-108">Beispiel 1: Abrufen einer Web App-Zugriffs Einschränkungs Konfiguration aus einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="370e5-108">Example 1: Get a Web App Access Restriction Config from a resource group</span></span>
```
PS C:\>Get-AzWebAppAccessRestrictionConfig -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="370e5-109">Dieser Befehl ruft die Zugriffs Beschränkungs Konfiguration einer Web-App mit dem Namen ContosoSite ab, die zur Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="370e5-109">This command gets the access restriction config of a Web App named ContosoSite that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="370e5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="370e5-110">PARAMETERS</span></span>

### <span data-ttu-id="370e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="370e5-111">-DefaultProfile</span></span>
<span data-ttu-id="370e5-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="370e5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="370e5-113">-Name</span><span class="sxs-lookup"><span data-stu-id="370e5-113">-Name</span></span>
<span data-ttu-id="370e5-114">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="370e5-114">WebApp Name</span></span>

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

### <span data-ttu-id="370e5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="370e5-115">-ResourceGroupName</span></span>
<span data-ttu-id="370e5-116">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="370e5-116">Resource Group Name</span></span>

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

### <span data-ttu-id="370e5-117">-Slotname</span><span class="sxs-lookup"><span data-stu-id="370e5-117">-SlotName</span></span>
<span data-ttu-id="370e5-118">Name des Bereitstellungs Steckplatzes.</span><span class="sxs-lookup"><span data-stu-id="370e5-118">Deployment Slot name.</span></span>

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

### <span data-ttu-id="370e5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="370e5-119">CommonParameters</span></span>
<span data-ttu-id="370e5-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="370e5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="370e5-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="370e5-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="370e5-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="370e5-122">INPUTS</span></span>

### <span data-ttu-id="370e5-123">System. String</span><span class="sxs-lookup"><span data-stu-id="370e5-123">System.String</span></span>

## <span data-ttu-id="370e5-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="370e5-124">OUTPUTS</span></span>

### <span data-ttu-id="370e5-125">Microsoft. Azure. Commands. webapps. Models. PSAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="370e5-125">Microsoft.Azure.Commands.WebApps.Models.PSAccessRestrictionConfig</span></span>

## <span data-ttu-id="370e5-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="370e5-126">NOTES</span></span>

## <span data-ttu-id="370e5-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="370e5-127">RELATED LINKS</span></span>

[<span data-ttu-id="370e5-128">Update-AzWebAppAccessRestrictionConfig</span><span class="sxs-lookup"><span data-stu-id="370e5-128">Update-AzWebAppAccessRestrictionConfig</span></span>](./Update-AzWebAppAccessRestrictionConfig.md)

[<span data-ttu-id="370e5-129">Add-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="370e5-129">Add-AzWebAppAccessRestrictionRule</span></span>](./Add-AzWebAppAccessRestrictionRule.md)

[<span data-ttu-id="370e5-130">Remove-AzWebAppAccessRestrictionRule</span><span class="sxs-lookup"><span data-stu-id="370e5-130">Remove-AzWebAppAccessRestrictionRule</span></span>](./Remove-AzWebAppAccessRestrictionRule.md)
