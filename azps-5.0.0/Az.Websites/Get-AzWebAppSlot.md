---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 100A5980-31E2-41F9-84D4-2F5F0CB78B8A
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappslot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSlot.md
ms.openlocfilehash: 4bd0e45df7f1c5c98b61f7f490a59a4c305c2c21
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175941"
---
# <span data-ttu-id="24e30-101">Get-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="24e30-101">Get-AzWebAppSlot</span></span>

## <span data-ttu-id="24e30-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="24e30-102">SYNOPSIS</span></span>
<span data-ttu-id="24e30-103">Ruft einen Azure Web App-Steckplatz ab.</span><span class="sxs-lookup"><span data-stu-id="24e30-103">Gets an Azure Web App slot.</span></span>

## <span data-ttu-id="24e30-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="24e30-104">SYNTAX</span></span>

### <span data-ttu-id="24e30-105">S1</span><span class="sxs-lookup"><span data-stu-id="24e30-105">S1</span></span>
```
Get-AzWebAppSlot [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="24e30-106">S2</span><span class="sxs-lookup"><span data-stu-id="24e30-106">S2</span></span>
```
Get-AzWebAppSlot [[-Slot] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="24e30-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="24e30-107">DESCRIPTION</span></span>
<span data-ttu-id="24e30-108">Das Cmdlet " **Get-AzWebAppSlot** " Ruft Informationen zu einem Azure Web App-Slot ab.</span><span class="sxs-lookup"><span data-stu-id="24e30-108">The **Get-AzWebAppSlot** cmdlet gets information about an Azure Web App Slot.</span></span>

## <span data-ttu-id="24e30-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="24e30-109">EXAMPLES</span></span>

### <span data-ttu-id="24e30-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="24e30-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppSlot -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard" -Slot "Slot001"
```

<span data-ttu-id="24e30-111">Dieser Befehl ruft den Steckplatz mit dem Namen Slot001 aus der Web-App mit dem Namen WebAppStandard ab, die zu der Ressourcengruppe Default-Web-westus gehört.</span><span class="sxs-lookup"><span data-stu-id="24e30-111">This command gets the slot named Slot001 from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="24e30-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="24e30-112">PARAMETERS</span></span>

### <span data-ttu-id="24e30-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24e30-113">-DefaultProfile</span></span>
<span data-ttu-id="24e30-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="24e30-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24e30-115">-Name</span><span class="sxs-lookup"><span data-stu-id="24e30-115">-Name</span></span>
<span data-ttu-id="24e30-116">Name des Webhosts</span><span class="sxs-lookup"><span data-stu-id="24e30-116">WebApp Name</span></span>

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

### <span data-ttu-id="24e30-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24e30-117">-ResourceGroupName</span></span>
<span data-ttu-id="24e30-118">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="24e30-118">Resource Group Name</span></span>

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

### <span data-ttu-id="24e30-119">-Slot</span><span class="sxs-lookup"><span data-stu-id="24e30-119">-Slot</span></span>
<span data-ttu-id="24e30-120">Name des webslots</span><span class="sxs-lookup"><span data-stu-id="24e30-120">WebApp Slot Name</span></span>

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

### <span data-ttu-id="24e30-121">-Webbasierte</span><span class="sxs-lookup"><span data-stu-id="24e30-121">-WebApp</span></span>
<span data-ttu-id="24e30-122">Webobjekt</span><span class="sxs-lookup"><span data-stu-id="24e30-122">WebApp Object</span></span>

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

### <span data-ttu-id="24e30-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24e30-123">CommonParameters</span></span>
<span data-ttu-id="24e30-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="24e30-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24e30-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24e30-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24e30-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="24e30-126">INPUTS</span></span>

### <span data-ttu-id="24e30-127">System. String</span><span class="sxs-lookup"><span data-stu-id="24e30-127">System.String</span></span>

### <span data-ttu-id="24e30-128">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="24e30-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="24e30-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="24e30-129">OUTPUTS</span></span>

### <span data-ttu-id="24e30-130">Microsoft. Azure. Commands. webapps. Models. PSSite</span><span class="sxs-lookup"><span data-stu-id="24e30-130">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="24e30-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="24e30-131">NOTES</span></span>

## <span data-ttu-id="24e30-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="24e30-132">RELATED LINKS</span></span>

[<span data-ttu-id="24e30-133">Neu – AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="24e30-133">New-AzWebAppSlot</span></span>](./New-AzWebAppSlot.md)

[<span data-ttu-id="24e30-134">Remove-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="24e30-134">Remove-AzWebAppSlot</span></span>](./Remove-AzWebAppSlot.md)

[<span data-ttu-id="24e30-135">Neustart-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="24e30-135">Restart-AzWebAppSlot</span></span>](./Restart-AzWebAppSlot.md)

[<span data-ttu-id="24e30-136">Satz-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="24e30-136">Set-AzWebAppSlot</span></span>](./Set-AzWebAppSlot.md)

[<span data-ttu-id="24e30-137">Anfang-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="24e30-137">Start-AzWebAppSlot</span></span>](./Start-AzWebAppSlot.md)

[<span data-ttu-id="24e30-138">Stopp-AzWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="24e30-138">Stop-AzWebAppSlot</span></span>](./Stop-AzWebAppSlot.md)

[<span data-ttu-id="24e30-139">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="24e30-139">Get-AzWebApp</span></span>](./Get-AzWebApp.md)
