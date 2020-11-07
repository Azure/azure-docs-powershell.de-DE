---
external help file: Microsoft.Azure.Commands.Management.PowerBIEmbedded.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/reset-azurermpowerbiworkspacecollectionaccesskeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.Management.PowerBIEmbedded/help/Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys.md
ms.openlocfilehash: cb8236acfc0fd1d349091593a2510da271820020
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664809"
---
# <span data-ttu-id="fdd7b-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="fdd7b-101">Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>

## <span data-ttu-id="fdd7b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fdd7b-102">SYNOPSIS</span></span>
<span data-ttu-id="fdd7b-103">Setzt die angegebene Zugriffstaste zurück.</span><span class="sxs-lookup"><span data-stu-id="fdd7b-103">Resets the specified access key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fdd7b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fdd7b-104">SYNTAX</span></span>

```
Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys [-ResourceGroupName] <String>
 [-WorkspaceCollectionName] <String> [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdd7b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fdd7b-105">DESCRIPTION</span></span>
<span data-ttu-id="fdd7b-106">Das Cmdlet **Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** setzt den angegebenen Zugriffsschlüssel in ihrer Power BI-Arbeitsbereichs Sammlung zurück.</span><span class="sxs-lookup"><span data-stu-id="fdd7b-106">The **Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="fdd7b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fdd7b-107">EXAMPLES</span></span>

### <span data-ttu-id="fdd7b-108">Beispiel 1: Zurücksetzen der primären Zugriffstaste</span><span class="sxs-lookup"><span data-stu-id="fdd7b-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzureRmPowerBIWorkspaceCollectionAccessKeys -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="fdd7b-109">Mit diesem Befehl wird die primäre Zugriffstaste für die Arbeitsbereichs Sammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="fdd7b-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="fdd7b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fdd7b-110">PARAMETERS</span></span>

### <span data-ttu-id="fdd7b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdd7b-111">-DefaultProfile</span></span>
<span data-ttu-id="fdd7b-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="fdd7b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fdd7b-113">-Key1</span><span class="sxs-lookup"><span data-stu-id="fdd7b-113">-Key1</span></span>
<span data-ttu-id="fdd7b-114">Gibt an, dass mit diesem Cmdlet die primäre Zugriffstaste zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="fdd7b-114">Indicates that this cmdlet resets the primary access key.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdd7b-115">-Key2</span><span class="sxs-lookup"><span data-stu-id="fdd7b-115">-Key2</span></span>
<span data-ttu-id="fdd7b-116">Gibt an, dass mit diesem Cmdlet die sekundäre Zugriffstaste zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="fdd7b-116">Indicates that this cmdlet resets the secondary access key.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdd7b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdd7b-117">-ResourceGroupName</span></span>
<span data-ttu-id="fdd7b-118">Gibt den Namen der Ressourcengruppe der Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="fdd7b-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="fdd7b-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="fdd7b-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="fdd7b-120">Gibt den Namen der Power BI-Arbeitsbereichs Sammlung an, für die dieses Cmdlet fungiert.</span><span class="sxs-lookup"><span data-stu-id="fdd7b-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdd7b-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fdd7b-121">-Confirm</span></span>
<span data-ttu-id="fdd7b-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fdd7b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdd7b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdd7b-123">-WhatIf</span></span>
<span data-ttu-id="fdd7b-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fdd7b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdd7b-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fdd7b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdd7b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdd7b-126">CommonParameters</span></span>
<span data-ttu-id="fdd7b-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdd7b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdd7b-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdd7b-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdd7b-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fdd7b-129">INPUTS</span></span>

### <span data-ttu-id="fdd7b-130">System. String</span><span class="sxs-lookup"><span data-stu-id="fdd7b-130">System.String</span></span>

## <span data-ttu-id="fdd7b-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fdd7b-131">OUTPUTS</span></span>

### <span data-ttu-id="fdd7b-132">Microsoft. Azure. Commands. Management. PowerBIEmbedded. Models. PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="fdd7b-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="fdd7b-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="fdd7b-133">NOTES</span></span>

## <span data-ttu-id="fdd7b-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fdd7b-134">RELATED LINKS</span></span>

[<span data-ttu-id="fdd7b-135">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span><span class="sxs-lookup"><span data-stu-id="fdd7b-135">Get-AzureRmPowerBIWorkspaceCollectionAccessKeys</span></span>](./Get-AzureRmPowerBIWorkspaceCollectionAccessKeys.md)


