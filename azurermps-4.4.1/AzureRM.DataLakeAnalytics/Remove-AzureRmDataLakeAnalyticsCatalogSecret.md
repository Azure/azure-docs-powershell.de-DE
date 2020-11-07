---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 7F063C03-3EAA-4D90-BC4B-E29721B328D9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsCatalogSecret.md
ms.openlocfilehash: 16716b0df5867832d51ed00797f19d5dfc0f0b1e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663979"
---
# <span data-ttu-id="8a9a9-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="8a9a9-101">Remove-AzureRmDataLakeAnalyticsCatalogSecret</span></span>

## <span data-ttu-id="8a9a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a9a9-102">SYNOPSIS</span></span>
<span data-ttu-id="8a9a9-103">Löscht einen Data Lake Analytics-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="8a9a9-103">Deletes a Data Lake Analytics secret.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a9a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a9a9-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeAnalyticsCatalogSecret [-Account] <String> [-DatabaseName] <String> [[-Name] <String>]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a9a9-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a9a9-105">DESCRIPTION</span></span>
<span data-ttu-id="8a9a9-106">Das Cmdlet **Remove-AzureRmDataLakeAnalyticsCatalogSecret** löscht einen Azure Data Lake-Analyse Katalog Secret.</span><span class="sxs-lookup"><span data-stu-id="8a9a9-106">The **Remove-AzureRmDataLakeAnalyticsCatalogSecret** cmdlet deletes an Azure Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="8a9a9-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a9a9-107">EXAMPLES</span></span>

### <span data-ttu-id="8a9a9-108">Beispiel 1: Entfernen eines Geheimnisses</span><span class="sxs-lookup"><span data-stu-id="8a9a9-108">Example 1: Remove a secret</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsCatalogSecret -Account "ContosoAdla" -DatabaseName "DatabaseName" -Name "SecretName"
```

<span data-ttu-id="8a9a9-109">Mit diesem Befehl wird der angegebene Data Lake-Analyse Katalog Secret entfernt.</span><span class="sxs-lookup"><span data-stu-id="8a9a9-109">This command removes the specified Data Lake Analytics catalog secret.</span></span>

## <span data-ttu-id="8a9a9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a9a9-110">PARAMETERS</span></span>

### <span data-ttu-id="8a9a9-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="8a9a9-111">-Account</span></span>
<span data-ttu-id="8a9a9-112">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="8a9a9-112">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a9a9-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8a9a9-113">-DatabaseName</span></span>
<span data-ttu-id="8a9a9-114">Gibt den Namen der Datenbank an, die den geheimen Schlüssel enthält.</span><span class="sxs-lookup"><span data-stu-id="8a9a9-114">Specifies the name of the database that holds the secret.</span></span>

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

### <span data-ttu-id="8a9a9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8a9a9-115">-Force</span></span>
<span data-ttu-id="8a9a9-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="8a9a9-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a9a9-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8a9a9-117">-Name</span></span>
<span data-ttu-id="8a9a9-118">Gibt den Namen des Geheimnisses an.</span><span class="sxs-lookup"><span data-stu-id="8a9a9-118">Specifies the name of the secret.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a9a9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a9a9-119">-PassThru</span></span>
<span data-ttu-id="8a9a9-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="8a9a9-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8a9a9-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="8a9a9-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a9a9-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8a9a9-122">-Confirm</span></span>
<span data-ttu-id="8a9a9-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a9a9-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a9a9-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a9a9-124">-WhatIf</span></span>
<span data-ttu-id="8a9a9-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a9a9-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a9a9-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a9a9-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a9a9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a9a9-127">-DefaultProfile</span></span>
<span data-ttu-id="8a9a9-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a9a9-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a9a9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a9a9-129">CommonParameters</span></span>
<span data-ttu-id="8a9a9-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a9a9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a9a9-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a9a9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a9a9-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a9a9-132">INPUTS</span></span>

## <span data-ttu-id="8a9a9-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a9a9-133">OUTPUTS</span></span>

### <span data-ttu-id="8a9a9-134">bool</span><span class="sxs-lookup"><span data-stu-id="8a9a9-134">bool</span></span>
<span data-ttu-id="8a9a9-135">Wenn passthru angegeben ist, gibt true nach Abschluss des Vorgangs zurück.</span><span class="sxs-lookup"><span data-stu-id="8a9a9-135">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="8a9a9-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a9a9-136">NOTES</span></span>

## <span data-ttu-id="8a9a9-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a9a9-137">RELATED LINKS</span></span>

[<span data-ttu-id="8a9a9-138">Neu – AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="8a9a9-138">New-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./New-AzureRmDataLakeAnalyticsCatalogSecret.md)

[<span data-ttu-id="8a9a9-139">Satz-AzureRmDataLakeAnalyticsCatalogSecret</span><span class="sxs-lookup"><span data-stu-id="8a9a9-139">Set-AzureRmDataLakeAnalyticsCatalogSecret</span></span>](./Set-AzureRmDataLakeAnalyticsCatalogSecret.md)


