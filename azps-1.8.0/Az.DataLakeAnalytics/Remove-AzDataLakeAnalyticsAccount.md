---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: AEAD985C-F342-4B24-9BFD-6448436FE9BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: 5e62bc19ec400f3dbfff3c089880cd14ce95609e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93820272"
---
# <span data-ttu-id="f6823-101">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f6823-101">Remove-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="f6823-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f6823-102">SYNOPSIS</span></span>
<span data-ttu-id="f6823-103">Löscht ein Data Lake Analytics-Konto.</span><span class="sxs-lookup"><span data-stu-id="f6823-103">Deletes a Data Lake Analytics account.</span></span>

## <span data-ttu-id="f6823-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6823-104">SYNTAX</span></span>

```
Remove-AzDataLakeAnalyticsAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6823-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6823-105">DESCRIPTION</span></span>
<span data-ttu-id="f6823-106">Mit dem Cmdlet **Remove-AzDataLakeAnalyticsAccount** wird ein Azure Data Lake-Analyse Konto endgültig gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f6823-106">The **Remove-AzDataLakeAnalyticsAccount** cmdlet permanently deletes an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="f6823-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6823-107">EXAMPLES</span></span>

### <span data-ttu-id="f6823-108">Beispiel 1: Entfernen eines Kontos</span><span class="sxs-lookup"><span data-stu-id="f6823-108">Example 1: Remove an account</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount"
```

<span data-ttu-id="f6823-109">Mit diesem Befehl wird das angegebene Data Lake Analytics-Konto entfernt.</span><span class="sxs-lookup"><span data-stu-id="f6823-109">This command removes the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="f6823-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6823-110">PARAMETERS</span></span>

### <span data-ttu-id="f6823-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6823-111">-DefaultProfile</span></span>
<span data-ttu-id="f6823-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f6823-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6823-113">-Force</span><span class="sxs-lookup"><span data-stu-id="f6823-113">-Force</span></span>
<span data-ttu-id="f6823-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="f6823-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6823-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f6823-115">-Name</span></span>
<span data-ttu-id="f6823-116">Gibt den Namen des Daten Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="f6823-116">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="f6823-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6823-117">-PassThru</span></span>
<span data-ttu-id="f6823-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f6823-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f6823-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="f6823-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f6823-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6823-120">-ResourceGroupName</span></span>
<span data-ttu-id="f6823-121">Gibt den Ressourcengruppennamen des Data Lake Analytics-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="f6823-121">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6823-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f6823-122">-Confirm</span></span>
<span data-ttu-id="f6823-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6823-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6823-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6823-124">-WhatIf</span></span>
<span data-ttu-id="f6823-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6823-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6823-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6823-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6823-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6823-127">CommonParameters</span></span>
<span data-ttu-id="f6823-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6823-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6823-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6823-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6823-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f6823-130">INPUTS</span></span>

### <span data-ttu-id="f6823-131">System. String</span><span class="sxs-lookup"><span data-stu-id="f6823-131">System.String</span></span>

## <span data-ttu-id="f6823-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f6823-132">OUTPUTS</span></span>

### <span data-ttu-id="f6823-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f6823-133">System.Boolean</span></span>

## <span data-ttu-id="f6823-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="f6823-134">NOTES</span></span>

## <span data-ttu-id="f6823-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f6823-135">RELATED LINKS</span></span>

[<span data-ttu-id="f6823-136">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f6823-136">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f6823-137">Neu – AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f6823-137">New-AzDataLakeAnalyticsAccount</span></span>](./New-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f6823-138">Satz-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f6823-138">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="f6823-139">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="f6823-139">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


