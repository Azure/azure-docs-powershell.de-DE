---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 4813EE2B-16C4-4716-B6DD-9447A0B46F3D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCallbackUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountCallbackUrl.md
ms.openlocfilehash: 6cbb37eb211c766959f2513abe3bbe1554bfdb23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479170"
---
# <span data-ttu-id="4f5cd-101">Get-AzureRmIntegrationAccountCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="4f5cd-101">Get-AzureRmIntegrationAccountCallbackUrl</span></span>

## <span data-ttu-id="4f5cd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4f5cd-102">SYNOPSIS</span></span>
<span data-ttu-id="4f5cd-103">Ruft eine Integrations Konto-Rückruf-URL ab.</span><span class="sxs-lookup"><span data-stu-id="4f5cd-103">Gets an integration account callback URL.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f5cd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f5cd-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountCallbackUrl -ResourceGroupName <String> -Name <String> [-NotAfter <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f5cd-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f5cd-105">DESCRIPTION</span></span>
<span data-ttu-id="4f5cd-106">Das Cmdlet " **Get-AzureRmIntegrationAccountCallbackUrl** " Ruft eine Integrations Konto-Rückruf-URL aus einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="4f5cd-106">The **Get-AzureRmIntegrationAccountCallbackUrl** cmdlet gets an integration account callback URL from a resource group.</span></span>
<span data-ttu-id="4f5cd-107">Dieses Cmdlet gibt ein **CallbackUrl** -Objekt zurück, das die Rückruf-URL für das Integrations Konto darstellt.</span><span class="sxs-lookup"><span data-stu-id="4f5cd-107">This cmdlet returns a **CallbackUrl** object that represents the integration account callback URL.</span></span>
<span data-ttu-id="4f5cd-108">Geben Sie den Namen des Integrations Kontos und die Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4f5cd-108">Specify the integration account name and resource group name.</span></span>

<span data-ttu-id="4f5cd-109">Dieses Modul unterstützt dynamische Parameter.</span><span class="sxs-lookup"><span data-stu-id="4f5cd-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4f5cd-110">Wenn Sie einen dynamischen Parameter verwenden möchten, geben Sie ihn in den Befehl ein.</span><span class="sxs-lookup"><span data-stu-id="4f5cd-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4f5cd-111">Wenn Sie die Namen der dynamischen Parameter ermitteln möchten, geben Sie nach dem Cmdlet-Namen einen Bindestrich (-) ein, und drücken Sie dann wiederholt die Tab-Taste, um die verfügbaren Parameter zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="4f5cd-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4f5cd-112">Wenn Sie einen erforderlichen Vorlagenparameter nicht angeben, werden Sie vom Cmdlet zur Eingabe des Werts aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="4f5cd-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4f5cd-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f5cd-113">EXAMPLES</span></span>

### <span data-ttu-id="4f5cd-114">Beispiel 1: Abrufen einer Integrations Konto-Rückruf-URL</span><span class="sxs-lookup"><span data-stu-id="4f5cd-114">Example 1: Get an integration account callback URL</span></span>
```
PS C:\>Get-AzureRmIntegrationAccountCallbackUrl -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -NotAfter "03/25/2016 18:23:22"
CallBackUrl : https://<baseurl>/integrationAccounts/8811f0155a364b5e9618ba28f7180601?api-version=2015-08-01-preview&se=2016-03
              -25T18%3A23%3A22.0000000Z&sp=%2F%2Fread&sv=1.0&sig=<value>
```

<span data-ttu-id="4f5cd-115">Dieser Befehl ruft eine Integrations Konto-Rückruf-URL ab.</span><span class="sxs-lookup"><span data-stu-id="4f5cd-115">This command gets an integration account callback URL.</span></span>

## <span data-ttu-id="4f5cd-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f5cd-116">PARAMETERS</span></span>

### <span data-ttu-id="4f5cd-117">-Name</span><span class="sxs-lookup"><span data-stu-id="4f5cd-117">-Name</span></span>
<span data-ttu-id="4f5cd-118">Gibt den Namen eines Integrations Kontos an.</span><span class="sxs-lookup"><span data-stu-id="4f5cd-118">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f5cd-119">-NotAfter</span><span class="sxs-lookup"><span data-stu-id="4f5cd-119">-NotAfter</span></span>
<span data-ttu-id="4f5cd-120">Gibt das Ablaufdatum für die Rückruf-URL an.</span><span class="sxs-lookup"><span data-stu-id="4f5cd-120">Specifies the expiry date for the callback URL.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4f5cd-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f5cd-121">-ResourceGroupName</span></span>
<span data-ttu-id="4f5cd-122">Gibt den Namen einer Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4f5cd-122">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f5cd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f5cd-123">-DefaultProfile</span></span>
<span data-ttu-id="4f5cd-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4f5cd-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f5cd-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f5cd-125">CommonParameters</span></span>
<span data-ttu-id="4f5cd-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f5cd-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f5cd-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f5cd-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f5cd-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4f5cd-128">INPUTS</span></span>

## <span data-ttu-id="4f5cd-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4f5cd-129">OUTPUTS</span></span>

### <span data-ttu-id="4f5cd-130">Microsoft. Azure. Management. Logic. Models. CallbackUrl</span><span class="sxs-lookup"><span data-stu-id="4f5cd-130">Microsoft.Azure.Management.Logic.Models.CallbackUrl</span></span>

## <span data-ttu-id="4f5cd-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="4f5cd-131">NOTES</span></span>

## <span data-ttu-id="4f5cd-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4f5cd-132">RELATED LINKS</span></span>

[<span data-ttu-id="4f5cd-133">Get-AzureRmLogicAppTriggerCallbackUrl</span><span class="sxs-lookup"><span data-stu-id="4f5cd-133">Get-AzureRmLogicAppTriggerCallbackUrl</span></span>](./Get-AzureRmLogicAppTriggerCallbackUrl.md)


