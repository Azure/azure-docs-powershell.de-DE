---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppSlot.md
ms.openlocfilehash: f7be5b7877362484d0f3dfe4d19b8afc669e917c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93475865"
---
# <span data-ttu-id="84996-101">Get-AzureRmWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="84996-101">Get-AzureRmWebAppSlot</span></span>

## <span data-ttu-id="84996-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="84996-102">SYNOPSIS</span></span>
<span data-ttu-id="84996-103">Ruft einen Azure Web App-Steckplatz ab.</span><span class="sxs-lookup"><span data-stu-id="84996-103">Gets an Azure Web App slot.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84996-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="84996-104">SYNTAX</span></span>

### <span data-ttu-id="84996-105">S1</span><span class="sxs-lookup"><span data-stu-id="84996-105">S1</span></span>
```
Get-AzureRmWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="84996-106">S2</span><span class="sxs-lookup"><span data-stu-id="84996-106">S2</span></span>
```
Get-AzureRmWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84996-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84996-107">DESCRIPTION</span></span>
<span data-ttu-id="84996-108">Das Cmdlet " **Get-AzureRmWebAppSlot** " Ruft Informationen zu einem Azure Web App-Slot ab.</span><span class="sxs-lookup"><span data-stu-id="84996-108">The **Get-AzureRmWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="84996-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="84996-109">EXAMPLES</span></span>

### <span data-ttu-id="84996-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="84996-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="84996-111">Dieser Befehl ruft den Steckplatz mit dem Namen Slot001 aus der Web-App mit dem Namen WebAppStandard ab, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="84996-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="84996-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="84996-112">PARAMETERS</span></span>

### <span data-ttu-id="84996-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84996-113">-DefaultProfile</span></span>
<span data-ttu-id="84996-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="84996-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84996-115">-Name</span><span class="sxs-lookup"><span data-stu-id="84996-115">-Name</span></span>
<span data-ttu-id="84996-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="84996-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84996-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84996-117">-ResourceGroupName</span></span>
<span data-ttu-id="84996-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="84996-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84996-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="84996-119">-Slot</span></span>
<span data-ttu-id="84996-120">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="84996-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="84996-121">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="84996-121">-WebApp</span></span>
<span data-ttu-id="84996-122">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="84996-122">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84996-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84996-123">CommonParameters</span></span>
<span data-ttu-id="84996-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84996-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84996-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84996-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84996-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="84996-126">INPUTS</span></span>

### <span data-ttu-id="84996-127">System. String</span><span class="sxs-lookup"><span data-stu-id="84996-127">System.String</span></span>

### <span data-ttu-id="84996-128">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="84996-128">Microsoft.Azure.Management.WebSites.Models.Site</span></span>
<span data-ttu-id="84996-129">Parameter: webByValue</span><span class="sxs-lookup"><span data-stu-id="84996-129">Parameters: WebApp (ByValue)</span></span>

## <span data-ttu-id="84996-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="84996-130">OUTPUTS</span></span>

### <span data-ttu-id="84996-131">Microsoft. Azure. Management. Websites. Models. Website</span><span class="sxs-lookup"><span data-stu-id="84996-131">Microsoft.Azure.Management.WebSites.Models.Site</span></span>

## <span data-ttu-id="84996-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="84996-132">NOTES</span></span>

## <span data-ttu-id="84996-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="84996-133">RELATED LINKS</span></span>

[<span data-ttu-id="84996-134">Neu – AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="84996-134">New-AzureRMWebAppSlot</span></span>](./New-AzureRMWebAppSlot.md)

[<span data-ttu-id="84996-135">Remove-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="84996-135">Remove-AzureRMWebAppSlot</span></span>](./Remove-AzureRMWebAppSlot.md)

[<span data-ttu-id="84996-136">Neustart-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="84996-136">Restart-AzureRMWebAppSlot</span></span>](./Restart-AzureRMWebAppSlot.md)

[<span data-ttu-id="84996-137">Satz-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="84996-137">Set-AzureRMWebAppSlot</span></span>](./Set-AzureRMWebAppSlot.md)

[<span data-ttu-id="84996-138">Anfang-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="84996-138">Start-AzureRMWebAppSlot</span></span>](./Start-AzureRMWebAppSlot.md)

[<span data-ttu-id="84996-139">Stopp-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="84996-139">Stop-AzureRMWebAppSlot</span></span>](./Stop-AzureRMWebAppSlot.md)

[<span data-ttu-id="84996-140">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="84996-140">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)
