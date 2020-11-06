---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 2D83D38F-3A5C-40DB-BE8B-D52E5CAFCF6E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppCertificate.md
ms.openlocfilehash: e2aaa6ed6e66e61f8d62f1235ff8e2a8ff9f65e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478149"
---
# <span data-ttu-id="7b12d-101">Get-AzureRmWebAppCertificate</span><span class="sxs-lookup"><span data-stu-id="7b12d-101">Get-AzureRmWebAppCertificate</span></span>

## <span data-ttu-id="7b12d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b12d-102">SYNOPSIS</span></span>
<span data-ttu-id="7b12d-103">Ruft ein Azure Web App-Zertifikat ab.</span><span class="sxs-lookup"><span data-stu-id="7b12d-103">Gets an Azure Web App certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b12d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b12d-104">SYNTAX</span></span>

```
Get-AzureRmWebAppCertificate [[-ResourceGroupName] <String>] [[-Thumbprint] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b12d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b12d-105">DESCRIPTION</span></span>
<span data-ttu-id="7b12d-106">Das Cmdlet " **Get-AzureRmWebAppCertificate** " Ruft Informationen zu Azure Web App-Zertifikaten ab, die einer angegebenen Ressourcengruppe zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7b12d-106">The **Get-AzureRmWebAppCertificate** cmdlet gets information about Azure Web App certificates associated with a specified resource group.</span></span>
<span data-ttu-id="7b12d-107">Wenn Sie den Fingerabdruck des Zertifikats kennen, können Sie dieses Cmdlet auch verwenden, um Informationen zu einem angegebenen Zertifikat abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7b12d-107">If you know the certificate thumbprint you can also use this cmdlet to get information about a specified certificate.</span></span>

## <span data-ttu-id="7b12d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b12d-108">EXAMPLES</span></span>

### <span data-ttu-id="7b12d-109">Beispiel 1: Abrufen von Web App-Zertifikaten in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="7b12d-109">Example 1: Get Web App certificates in a resource group</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="7b12d-110">Dieser Befehl gibt Informationen zu den geuploadeten Web App-Zertifikaten zurück, die der Ressourcengruppe ContosoResourceGroup zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="7b12d-110">This command returns information about the uploaded Web App certificates associated with the resource group ContosoResourceGroup.</span></span>

### <span data-ttu-id="7b12d-111">Beispiel 2: Abrufen eines angegebenen Web App-Zertifikats</span><span class="sxs-lookup"><span data-stu-id="7b12d-111">Example 2: Get a specified web app certificate</span></span>
```
PS C:\>Get-AzureRmWebAppCertificate -ResourceGroupName "ContosoResourceGroup" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3"
```

<span data-ttu-id="7b12d-112">Dieser Befehl ruft das ContosoResourceGroup Web App-Zertifikat mit dem Fingerabdruck-E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span><span class="sxs-lookup"><span data-stu-id="7b12d-112">This command gets the ContosoResourceGroup Web App certificate with the thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3.</span></span>

## <span data-ttu-id="7b12d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b12d-113">PARAMETERS</span></span>

### <span data-ttu-id="7b12d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b12d-114">-DefaultProfile</span></span>
<span data-ttu-id="7b12d-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7b12d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b12d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b12d-116">-ResourceGroupName</span></span>
<span data-ttu-id="7b12d-117">Gibt den Namen der Ressourcengruppe an, der das Zertifikat zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="7b12d-117">Specifies the name of the resource group that the certificate is assigned to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b12d-118">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="7b12d-118">-Thumbprint</span></span>
<span data-ttu-id="7b12d-119">Gibt den eindeutigen Bezeichner für das Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="7b12d-119">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b12d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b12d-120">CommonParameters</span></span>
<span data-ttu-id="7b12d-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b12d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b12d-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b12d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b12d-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b12d-123">INPUTS</span></span>

### <span data-ttu-id="7b12d-124">Keine</span><span class="sxs-lookup"><span data-stu-id="7b12d-124">None</span></span>
<span data-ttu-id="7b12d-125">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="7b12d-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7b12d-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b12d-126">OUTPUTS</span></span>

## <span data-ttu-id="7b12d-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b12d-127">NOTES</span></span>

## <span data-ttu-id="7b12d-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b12d-128">RELATED LINKS</span></span>

[<span data-ttu-id="7b12d-129">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="7b12d-129">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)


